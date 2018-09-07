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


