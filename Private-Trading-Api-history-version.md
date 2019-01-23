## Private Trading Api history version

This page is for users who used V1 version. New users could use the new version directly, click to check latest version of [Private Trading Api](/cointiger/api-docs-en/wiki/REST-Api-List)

### Private Trading API

When using Private Trading API, users need to apply Api Key and Secret on CoinTiger to sign, Trading AOI history version sign rules.

| Foundation                              | API                                   | Details                                                      |
| --------------------------------------- | ------------------------------------- | ------------------------------------------------------------ |
| Create orders                           | POST {Trading_Macro}/api/order        | [Check](/cointiger/api-docs-en/wiki/Trading-Create-Order)    |
| Cancel orders                           | DELETE {Trading_Macro}/api/order      | [Check](/cointiger/api-docs-en/wiki/Trading-Cancel-Order)    |
| Require current orders                  | GET {Trading_Macro}/api/order/new     | [Check](/cointiger/api-docs-en/wiki/Trading-Get-The-Current-Commission) |
| Require history orders                  | GET {Trading_Macro}/api/order/history | [Check](/cointiger/api-docs-en/wiki/Trading-Get-The-History-Commissioned) |
| Require history transaction information | GET {Trading_Macro}/api/order/trade   | [Check](/cointiger/api-docs-en/wiki/Trading-Get-The-Transaction-Record) |
| Require Balance information             | GET {Trading_Macro}/api/user/balance  | [Check](/cointiger/api-docs-en/wiki/Trading-Get-The-Fund-Information) |

 

 