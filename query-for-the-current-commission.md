#### GET {Trading_Macro_v2}/order/current
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
GET https://api.cointiger.com/exchange/trading/api/v2/order/current?api_key=c9a97adf-7909-444a-bf9e-1471210c4777&symbol=ethbtc&start-date=2018-02-11&end-date=2018-04-11&direct=prev&from=4887374&states=filled,part_filled,pending_cancel&size=10&sign=b84ceabfbe5c9975fde698279ab90cf6a9b39eae6fe0951455d748428b95345eb0a9d41075c5e7d66061e29fc2064c62ccd98a93fa7b885fa965c9e10fbdee99&types=buy-market&time=1525515995127
```

Response Data:



| parameter subject | must or no | type   | describtion       | ranges                                                       |
| ----------------- | ---------- | ------ | ----------------- | ------------------------------------------------------------ |
| id                | true       | string | order ID          |                                                              |
| user_id           | true       | long   | account ID        |                                                              |
| volume            | true       | string | order amount      |                                                              |
| deal_volume       | false      | string | deal amount       |                                                              |
| deal_money        | true       | string | deal capital      |                                                              |
| fee               | true       | string | fees              |                                                              |
| price             | true       | string | price             |                                                              |
| status            | false      | string | order status      | 1 ：new order, 2：compeletely deal,  3 ：partial deal ,  4：cancelled，6：abnormal order |
| type              | true       | string | order type        | buy-market, sell-market, buy-limit, sell-limit               |
| source            | true       | string | order source      | api                                                          |
| symbol            | true       | string | trading pairs     | btcbitcny, eoseth, ethbtc ...                                |
| ctime             | true       | string | create order time |                                                              |
| mtime             | true       | string | last deal         |                                                              |
响应例子: (example)

```
{
    "code": "0",
    "msg": "suc",
    "data": [
          {
            "symbol": "ethbtc",
            "fee": "0.00100000",
            "avg_price": "0.07231094",
            "source": 1,
            "type": "buy-limit",
            "mtime": 1524823324000,
            "volume": "1.000",
            "user_id": 10278,
            "price": "0.07231094",
            "ctime": 1524823301000,
            "deal_volume": "1.00000000",
            "id": 5228948,
            "deal_money": "0.07231094",
            "status": 2
        },
        ...
    ]
}
```