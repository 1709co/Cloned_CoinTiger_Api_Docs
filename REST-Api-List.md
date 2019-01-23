There are two limits of authority of REST API,  market information and transaction information

### Public API

Users could require latest market information through Public API. Public API is public for all API users

| Function                                                     | API                                                          | Details                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Require all transaction information                          | GET {Trading_Macro_v2}/currencys                             | [Check](/cointiger/api-docs-en/wiki/currencys-（V2）)        |
| Check current system time                                    | GET {Trading_Macro_v2}/timestamp                             | [Check](/cointiger/api-docs-en/wiki/query-the-current-time-of-the-system) |
| Require latest 24 hours market information of all coins      | GET [https://www.cointiger.com/exchange/api/public/market/detail](https://github.com/cointiger/api-docs-en/wiki/market-price-lastest-24hours-%EF%BC%88Applicable-for-the-market-price-display%EF%BC%89) | [Check](/cointiger/api-docs-en/wiki/market-price-lastest-24hours-（Applicable-for-the-market-price-display）) |
| Require latest 24 hours market information of single trading pair | GET {Market_Macro}/market/detail                             | [Check](/cointiger/api-docs-en/wiki/REST-market-price-lastest-24hours) |
| Require history transaction data of single trading pair      | GET{Market_Macro}/market/history/trade                       | [Check](/cointiger/api-docs-en/wiki/REST-transaction-history-data) |
| Require history K Line data of single trading pair           | GET{Market_Macro}/market/history/kline                       | [Check](/cointiger/api-docs-en/wiki/REST-k-line-history-data) |
| Require market information of single trading pair            | GET {Market_Macro}/market/depth                              | [Check](/cointiger/api-docs-en/wiki/REST-volume-depth)       |

 

### Private Trading API

Uses need to sign with API KEY and API Secret applied on CoinTiger, when using Private Trading API.   Sign rules

| Function                                                    | API                                        | Details                                                      |
| ----------------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------ |
| Create order                                                | POST {Trading_Macro_v2}/order              | [Check](/cointiger/api-docs-en/wiki/Create-Order-(V2))       |
| Cancel bunch of orders                                      | POST {Trading_Macro_v2}/order/batch_cancel | [Check](/cointiger/api-docs-en/wiki/Bulk-cancel-orders（V2）) |
| Check current orders and history orders                     | GET {Trading_Macro_v2}/order/orders        | [Check](/cointiger/api-docs-en/wiki/query-for-the-current-commission,-history-commision-(V2)) |
| Check current transaction data and history transaction data | GET {Trading_Macro_v2}/order/match_results | [Check](/cointiger/api-docs-en/wiki/Get-The-Transaction-Record-(V2)) |
| Check transaction details                                   | GET {Trading_Macro_v2}/order/make_detail   | [Check](/cointiger/api-docs-en/wiki/check-the-transaction-details-of-order-(V2)) |
| Check orders information                                    | GET {Trading_Macro_v2}/order/details       | [Check](/cointiger/api-docs-en/wiki/check-the-transaction-details-of-order-(V2)) |
| Check balance                                               | GET {Trading_Macro}/api/user/balance       | [Check](/cointiger/api-docs-en/wiki/Trading-Get-The-Fund-Information) |

Private Trading used to be updated, the new vision of [Private Trading Api](/cointiger/api-docs-en/wiki/REST-Api-List) could  Compatible with older versions, new users could use new version directly.  Users who used older version could check through clicking [Private Trading API](/cointiger/api-docs-en/wiki/Private-Trading-Api-history-version) old version