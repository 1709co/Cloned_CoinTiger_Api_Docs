#### GET {Trading_Macro_v2}/order/now（query for the current commission）
Request parameters
| parameter subject | must or not | type   | describtion                                                  | defaults                                      | ranges                             |
| ----------------- | ----------- | ------ | ------------------------------------------------------------ | --------------------------------------------- | ---------------------------------- |
| symbol            | true        | string | trading pairs                                                |                                               | btcbitcny, bchbtc, eoseth ...      |
| types             | false       | string | query for oerder types combinatio，use for segment   (whole) | buy-market, sell-market, buy-limi, sell-limit |                                    |
| states            | true        | string | query for oerder types combinatio，use for segment           |                                               | new ,  part_filled                 |
| from              | false       | string | query for start ID order ID                                  |                                               |                                    |
| direct            | false       | string | query direction                                              | next                                          | prev (forewards)，next (backwards) |
| size              | false       | string | query for record amount                                      | 50                                            | query 50 record maximum at once    |
| time              | true        | string | current timestamp                                            |                                               |                                    |


request parameters：example  (can not be used directly, need to replace your own parameters)

```
GET https://api.cointiger.com/exchange/trading/api/v2/order/now?api_key=c9a97adf-7909-444a-bf9e1471210c4777&symbol=ethbtc&direct=prev&from=4887374&states=filled,part_filled,pending_cancel&size=10&sign=b84ceabfbe5c9975fde698279ab90cf6a9b39eae6fe0951455d748428b95345eb0a9d41075c5e7d66061e29fc2064c62ccd98a93fa7b885fa965c9e10fbdee99&types=buy-market&time=1525515995127
```

