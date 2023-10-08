
# [L-3] Loss of precision

## Vulnerability Details

Division by large numbers may result in the result being zero, due to solidity not supporting fractions.

## Lines of code

### Total -> 148

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/ComptrollerStorage.sol#L145
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L137
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L138
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L201
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L429
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L430
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L331
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L332
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L345
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L346
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L347
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L348
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L364
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L365
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L366
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L154
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/JumpRateModel.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/WhitePaperInterestRateModel.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L65
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L67
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L297
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L438
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L481
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/lib/PancakeLibrary.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/lib/PancakeLibrary.sol#L103
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/lib/PancakeLibrary.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L501
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L585
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L654
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L881
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L882
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L885
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L886
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L889
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L893
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L922
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L949
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L972
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L1004
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L1009
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L1010
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L1012
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L1013
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath.sol#L49
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L121
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L122
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L126
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L130
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L134
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L163
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L165
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L167
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L169
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L171
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L173
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L175
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L177
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L179
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L181
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L183
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L185
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L187
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L189
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L191
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L193
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L195
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L197
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L199
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L214
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L220
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L226
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L232
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L238
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L244
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L250
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L256
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/Scores.sol#L13
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/Scores.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L86
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L88
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L152
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L153
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L154
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L664
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L759
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L864
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1337
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1586
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1617
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/CarefulMath.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/CarefulMath.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Exponential.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Exponential.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Exponential.sol#L175
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L13
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L123
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L135
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L143
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ExponentialNoError.sol#L189
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/SafeCast.sol#L4
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/SafeMath.sol#L93
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/SafeMath.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/SafeMath.sol#L117
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/SafeMath.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L58
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L328
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L439
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L175
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L43
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L209
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L224
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L204
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L213
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L228
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L238
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L209
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L224
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L209
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L224
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L234

## Impact
Division by large numbers may result in the result being zero, due to solidity not supporting fractions.


## Recommended Mitigation Steps

Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator.


# [L-4] `Initialization` can be front-run

## Vulnerability Details

The `initialize()` functions below are not called by another contract atomically after the contract is deployed, so it's possible for a `malicious user` to call `initialize()` which, if it's noticed in time, would require the project to re-deploy the contract in order to properly initialize.

## Lines of code

### Total -> 16

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L58
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L162
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/interfaces/IPancakePair.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L130
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L77
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L153
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L314
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/LiquidatorHarness.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L218
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L24

## Impact
A malicious user can call this to take ownership of this contract.


## Recommended Mitigation Steps

Consider creating a factory contract, which will `new` and `initialize()` each contract atomically.

# [L-5] Use `Ownable2Step` rather than `Ownable`

## Vulnerability Details

[Ownable2Step](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/3d7a93876a2e5e1d7fe29b5a0e96e222afdc4cfa/contracts/access/Ownable2Step.sol#L31-L56) and [Ownable2StepUpgradeable](https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/25aabd286e002a1526c345c8db259d57bdf0ad28/contracts/access/Ownable2StepUpgradeable.sol#L47-L63) prevent the contract ownership from mistakenly being transferred toan address that cannot handle it (e.g. due to a typo in the address), by requiring that the recipient of the owner permissions actively accept via a contract call of its own.

## Lines of code

### Total -> 38

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/VTreasury.sol#L12
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L21
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L70
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L247
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L250
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L251
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L254
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L261
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L313
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L389
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L460
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L463
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L522
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L535
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L538
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L550
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L309
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L337
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L343
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L288
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L313
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L341
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L347
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L309
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L337
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L343
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L309
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L337
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L343

## Impact
Contract ownership can be transferred to an address that cannot handle it.


## Recommended Mitigation Steps

Use `Ownable2Step` instead of `Ownable`.

# [L-6] Upgradeable contract is missing a `__gap[50]` storage variable to allow for new storage variables in later versions

## Vulnerability Details

See this [link](https://docs.openzeppelin.com/contracts/4.x/upgradeable#storage_gaps) for a description of this storage variable. While some contracts may not currently be sub-classed, adding the variable now protects against forgetting to add it in the future.

## Lines of code

### Total -> 50

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L86
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L103
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Interfaces.sol#L5
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L249
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L258
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L141
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L227
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L247
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L248
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L249
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L680
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L204
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L216
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L259
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/Scores.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L61
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L70
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L198
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L203
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L212
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L261
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L266
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L275
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultErrorReporter.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultErrorReporter.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultErrorReporter.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultErrorReporter.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultErrorReporter.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultErrorReporter.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L363
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L442

## Impact
This is empty reserved space in storage that is put in place in Upgradeable contracts. It allows us to freely add new state variables in the future without compromising the storage compatibility with existing deployments.


## Recommended Mitigation Steps

# TODO: manual review
.//before
contract Base {
    uint256 base1;
    uint256 base2;
}

//after

contract Base {
    uint256 base1;
    uint256[49] __gap;
}

contract Child is Base {
    uint256 child;
}
Reference: https://docs.openzeppelin.com/upgrades-plugins/1.x/writing-upgradeable#modifying-your-contracts

# [N-7] `public functions not called by the contract should be declared external instead`

## Vulnerability Details

Contracts are allowed to override their parents' functions and change the visibility from `external` to `public`.
## Lines of code

### Total -> 414

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/ComptrollerInterface.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L83
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L212
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L253
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L289
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L293
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L315
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L319
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L350
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L355
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L360
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L365
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L213
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L235
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L254
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L290
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L294
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L316
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L320
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L351
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L356
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L361
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L366
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L317
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegator.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L65
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/JumpRateModel.sol#L63
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/JumpRateModel.sol#L79
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/WhitePaperInterestRateModel.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/WhitePaperInterestRateModel.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/SnapshotLens.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/VenusLens.sol#L137
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/VenusLens.sol#L249
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/VenusLens.sol#L300
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L388
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L554
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L597
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L249
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L276
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L413
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L533
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L568
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L580
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L595
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L628
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L681
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L760
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L768
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIControllerInterface.sol#L6
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIControllerInterface.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIControllerInterface.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L83
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L154
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L167
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L197
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L97
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L157
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L63
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L153
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegate.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegate.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L421
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L431
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L441
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L454
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L478
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L495
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L507
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L353
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L364
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L479
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L504
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L519
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L530
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L265
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L267
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L270
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L273
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L275
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L277
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L347
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L352
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L154
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L167
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L197
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L65
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L217
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L222
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L49
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L93
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L117
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L136
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Ownable.sol#L62
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Owned.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Tokenlock.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Tokenlock.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L297
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L86
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L129
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L189
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L142
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L146
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L150
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L40
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L76
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L93
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L121
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L137
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L145
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L174
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L178
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L182
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L186
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L190
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerHarness.sol#L194
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerMock.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L12
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L65
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerScenario.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Const.sol#L6
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Const.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Const.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Const.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Counter.sol#L7
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Counter.sol#L11
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Counter.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Counter.sol#L21
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Counter.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/DiamondHarness.sol#L7
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/DiamondHarnessInterface.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L315
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L326
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L336
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L355
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L396
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L451
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L481
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L492
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L94
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L118
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L122
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L126
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L137
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L141
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L146
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L159
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L164
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L168
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L172
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L176
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L191
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L195
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L199
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L203
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L207
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L116
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L121
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Fauceteer.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FeeToken.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FeeToken.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FixedPriceOracle.sol#L12
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FixedPriceOracle.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/GovernorAlphaHarness.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/InterestRateModelHarness.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/InterestRateModelHarness.sol#L22
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/InterestRateModelHarness.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/LiquidatorHarness.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockMCD.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockMCD.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockMCD.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/SimplePriceOracle.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/SimplePriceOracle.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/SimplePriceOracle.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Structs.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Structs.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/TimelockHarness.sol#L12
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/TimelockHarness.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/TimelockHarness.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/TimelockHarness.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L55
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L63
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIHarness.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIHarness.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIHarness.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIHarness.sol#L22
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIHarness.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L58
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L62
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L82
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L86
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L92
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L97
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L119
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L132
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L136
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L159
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L163
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L167
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L196
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L267
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L271
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L302
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L306
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L310
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L318
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L322
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L326
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L330
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L334
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L338
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L344
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L349
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L353
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L358
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L371
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L376
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L380
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L384
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L388
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L403
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L407
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L411
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L415
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L419
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L427
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L431
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L442
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L446
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L450
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L60
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L69
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L40
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L91
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L100
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L115
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L129
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L154
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L175
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L187
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L215
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L282
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L291
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L335
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L347
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L367
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L414
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L422
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L435
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L439
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L443
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L447
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L451
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L478
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L485
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L552
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L556
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L560
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L567
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVestingHarness.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVestingHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVestingHarness.sol#L40
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVestingHarness.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L320
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L329
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L473
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L492
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L509
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L517
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L305
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L324
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L333
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L477
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L496
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L513
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L521
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L320
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L329
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L473
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L492
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L509
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L517
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L320
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L329
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L473
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L492
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L509
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L517

## Impact


## Recommended Mitigation Steps



# [N-8] Event is not properly `indexed`.

## Vulnerability Details

Index event fields make the field more quickly accessible to [off-chain tools](https://ethereum.stackexchange.com/questions/40396/can-somebody-please-explain-the-concept-of-event-indexing) that parse events.This is especially useful when it comes to filtering based on an address. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields).
## Lines of code

### Total -> 362

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L21
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L486
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L498
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L60
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L69
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L81
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L221
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L245
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/XVSRewardsHelper.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/XVSRewardsHelper.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L130
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L134
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L130
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L134
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L5
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L6
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L40
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L43
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L49
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L55
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoInterfaces.sol#L58
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L11
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/VTreasury.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/VTreasury.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/VTreasury.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/VTreasury.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/JumpRateModel.sol#L13
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/InterestRateModels/WhitePaperInterestRateModel.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Lens/ComptrollerLens.sol#L88
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L49
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L69
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L75
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L76
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L79
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L81
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L84
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L87
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L88
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L91
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L195
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L239
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L287
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L316
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L333
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L349
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L362
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L376
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L69
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/interfaces/IPancakePair.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/interfaces/IPancakePair.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L63
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L82
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L174
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L187
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L212
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L247
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L283
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L307
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L60
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L63
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L84
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L355
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/lib.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/lib.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L192
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L43
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L60
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L61
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L71
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L97
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L123
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L138
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L71
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L83
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L96
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L145
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L156
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L180
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L181
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L209
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L225
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L345
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L363
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L478
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L598
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L618
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L688
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L711
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L783
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L955
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1050
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1166
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1289
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1359
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1513
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L130
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L135
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L138
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L140
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L143
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L145
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L148
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L150
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L153
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L158
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L160
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L163
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L165
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L176
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L178
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L181
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L183
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L186
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L188
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L191
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L193
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L196
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L198
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L201
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L203
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L206
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L211
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L216
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L221
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L223
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VTokenInterfaces.sol#L326
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L192
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L23
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Context.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L58
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/ErrorReporter.sol#L263
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Tokenlock.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Tokenlock.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L21
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L14
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L22
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultErrorReporter.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L22
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L24
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L44
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L56
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L60
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L69
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L75
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L81
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L82
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultErrorReporter.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L10
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L20
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L25
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/LiquidatorHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L160
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L161
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L169
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L170
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L178
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L179
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L187
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L188
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockProtocolShareReserve.sol#L195
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L67
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L68
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L79
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L81
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L91
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L100
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/SimplePriceOracle.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L277
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L278
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L315
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L390
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L391
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L520
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L442
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L484
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L548
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L566
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L113
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L446
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L471
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L488
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L552
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L570
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L442
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L484
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L548
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L566
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L442
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L484
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L548
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L566

## Impact


## Recommended Mitigation Steps

Where applicable, each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three applicable fields, all of the applicable fields should be indexed.

# [N-9] Usually lines in source code are limited to [80 characters](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width)
.

## Vulnerability Details

{no_of_line}
## Lines of code

### Total -> 114

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/ComptrollerStorage.sol#L168
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/ComptrollerStorage.sol#L171
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/ComptrollerStorage.sol#L203
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L139
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L276
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L142
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/RewardFacet.sol#L183
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L291
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L292
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L294
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L311
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L312
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L314
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L79
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L8
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L456
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L234
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L394
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L412
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L435
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L443
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L142
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L148
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L172
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L190
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L196
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L220
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L244
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L267
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L289
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L314
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L337
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L355
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L361
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L385
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L402
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L408
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L431
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L455
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L479
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L501
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L524
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L541
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L546
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L571
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L592
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L834
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L775
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L902
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L928
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L213
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L105
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L110
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L115
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/libs/FixedMath0x.sol#L136
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L64
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L216
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L256
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L267
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L282
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L626
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L79
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L129
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L213
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L214
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L246
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L275
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L127
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L152
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L213
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L229
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L507
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L610
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L627
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L703
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L708
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L721
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L829
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L830
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1062
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1078
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1095
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1181
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1190
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1196
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1211
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1405
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1418
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1544
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1552
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L107
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L81
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L380
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L227
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L228
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L519

## Impact


## Recommended Mitigation Steps



# [N-10] Gas griefing/theft is possible on an unsafe external call

## Vulnerability Details

A low-level call will copy any amount of bytes to local memory. When bytes are copied from return data to memory, the memory expansion cost is paid. This means that when using a standard solidity call, the callee can `returnbomb` the caller, imposing an arbitrary gas cost. Because this gas is paid by the caller and in the caller's context, it can cause the caller to run out of gas and halt execution.
## Lines of code

### Total -> 1

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/lib/TransferHelper.sol#L61

## Impact


## Recommended Mitigation Steps

Consider replacing all unsafe call with excessivelySafeCall from this [repository](https://github.com/nomad-xyz/ExcessivelySafeCall).

# [N-11] No access control on `receive`/`payable` fallback

## Vulnerability Details

Users may send ETH by mistake to these contracts. As there is no access control on these functions, the funds will be permanently lost.
## Lines of code

### Total -> 1

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L92

## Impact


## Recommended Mitigation Steps



# [N-12] Use a `modifier` instead of `require` to check for `msg.sender`

## Vulnerability Details

If some functions are only allowed to be called by some specific users, consider using a `modifier` instead of checking with a `require` statement, especially if this check is done in multiple functions.
## Lines of code

### Total -> 441

- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/Diamond.sol#L38
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L61
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/FacetBase.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L126
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L135
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L143
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L148
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L152
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L166
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/MarketFacet.sol#L209
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/PolicyFacet.sol#L117
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Diamond/facets/SetterFacet.sol#L423
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Comptroller/Unitroller.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L105
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/DelegateBorrowers/SwapDebtDelegate.sol#L135
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L150
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L162
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L181
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L200
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L259
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L316
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L351
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L356
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L361
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha.sol#L366
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L163
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L182
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L201
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L260
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L317
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L352
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L357
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L362
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorAlpha2.sol#L367
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L51
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L138
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L157
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L178
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L265
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L266
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L350
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L360
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L418
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L432
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L447
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L461
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L474
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegate.sol#L480
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegator.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegator.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/GovernorBravoDelegator.sol#L43
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/IAccessControlManager.sol#L6
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L67
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L87
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L107
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Governance/Timelock.sol#L122
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L207
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L228
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L250
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L259
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L273
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Liquidator/Liquidator.sol#L274
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L220
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L226
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L248
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L294
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/PegStability/PegStability.sol#L308
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L140
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L142
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L144
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L146
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L176
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L179
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L210
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L220
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L233
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L235
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L259
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L264
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L290
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L291
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L317
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/RouterHelper.sol#L326
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L93
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L467
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L512
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L537
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L562
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L584
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L601
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L605
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L613
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L636
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L714
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L737
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L765
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L787
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L816
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L862
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L864
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L877
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L879
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Swap/SwapRouter.sol#L944
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/EIP20Interface.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/EIP20NonStandardInterface.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L398
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L399
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L401
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L403
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L404
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L434
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/Prime.sol#L453
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/Prime/PrimeLiquidityProvider.sol#L193
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L68
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L82
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L87
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L88
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L89
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L105
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L107
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L115
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L116
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L122
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAI.sol#L126
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L89
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L206
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L272
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L381
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L512
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L773
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIController.sol#L790
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/VAIUnitroller.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VAI/lib.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L96
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L119
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRT.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L152
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L153
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverter.sol#L158
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L64
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L94
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L135
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L149
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VRT/VRTConverterProxy.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L87
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20.sol#L88
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegate.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegate.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L186
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L258
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L299
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Delegator.sol#L403
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VBep20Immutable.sol#L33
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L139
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L147
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L159
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L176
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L184
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L322
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L481
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L619
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L712
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L806
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L822
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1071
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1087
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1201
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1308
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1375
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1398
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1442
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1453
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1470
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/VTokens/VToken.sol#L1517
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L96
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L98
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L119
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L151
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVS.sol#L155
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L46
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L115
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L116
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVesting.sol#L223
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L50
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L96
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L119
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Tokens/XVS/XVSVestingProxy.sol#L138
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Context.sol#L6
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Context.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Owned.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Utils/Owned.sol#L13
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L57
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L108
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L118
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L128
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L207
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L243
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L244
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVault.sol#L304
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L45
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L73
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L83
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L89
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L112
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L125
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/VRTVault/VRTVaultProxy.sol#L131
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L67
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L77
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L85
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L90
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L94
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L99
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L107
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVault.sol#L217
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L97
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/Vault/VAIVaultProxy.sol#L103
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L40
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L65
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L84
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSStore.sol#L89
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L100
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L133
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L143
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L277
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L279
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L284
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L285
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L288
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L294
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L298
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L301
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L407
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L408
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L422
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L425
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L431
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L435
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L470
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L474
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L483
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L494
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L501
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L504
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L505
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L689
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L693
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVault.sol#L847
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L48
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L97
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/XVSVault/XVSVaultProxy.sol#L103
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L52
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L59
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L61
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L74
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L75
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L102
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L109
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L111
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L115
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L122
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L123
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L159
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L161
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/BEP20.sol#L170
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerMock.sol#L13
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/ComptrollerMock.sol#L17
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilToken.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilToken.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilToken.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L187
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L363
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXDelegator.sol#L416
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L80
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/EvilXToken.sol#L208
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L75
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L87
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L117
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L126
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FaucetToken.sol#L136
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Fauceteer.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FeeToken.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FeeToken.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/FeeToken.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L67
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L72
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L77
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockDeflationaryToken.sol#L78
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L31
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L93
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/MockVBNB.sol#L140
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Structs.sol#L18
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/Structs.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/TimelockHarness.sol#L27
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VAIControllerHarness.sol#L11
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L168
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20Harness.sol#L420
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L66
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VBep20MockDelegate.sol#L124
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L7
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L11
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTConverterHarness.sol#L12
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L15
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/VRTVaultHarness.sol#L16
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L29
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L30
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L34
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L35
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L36
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L37
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L41
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L47
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L53
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L54
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBNB.sol#L55
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L104
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L106
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L156
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L161
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L167
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L176
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L177
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L201
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L202
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L216
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L218
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L220
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L222
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L265
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L272
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L325
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L368
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/WBTC.sol#L470
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSHarness.sol#L11
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSHarness.sol#L19
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSHarness.sol#L26
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVaultScenario.sol#L28
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVaultScenario.sol#L32
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVaultScenario.sol#L39
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVaultScenario.sol#L42
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/XVSVestingHarness.sol#L9
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L360
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L362
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L502
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BTC.sol#L507
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L105
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L118
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L364
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L366
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L506
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20BitcoinCash.sol#L511
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L360
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L362
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L502
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20Ethereum.sol#L507
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L101
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L114
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L360
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L362
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L502
- https://github.com/code-423n4/2023-09-venus/blob/main/./contracts/test/assets/BEP20XRP.sol#L507

## Impact


## Recommended Mitigation Steps

