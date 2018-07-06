#### GET {Trading_Macro_v2}/order/details

Request parameters：

| parameter name | whether necessary | type  | description       | default  | date range  |
| -------- | -------- | ------ | ----------------- | ------ | -------- |
| api_key  | true     | string | api key distributed by platform |        |          |
| symbol   | true     | string | trading pairs      |        |          |
| order_id | true     | string | order id    |        |          |
| sign     | true     | string | signature     |        |          |
| time     | true     | string | current timestamp   |        |          |

Request parameters: example (cannot be used directly, you need to replace your own parameters)

```
GET https://api.cointiger.com/exchange/trading/api/v2/order/details?api_key=100280001&time=1525522215129&order_id=4887370&symbol=ethbtc&sign=74d7439cc46211e925f0dcdd97fa000e75372e87a12e0804989ca575422e8935f68201c47f5d74ba3b1d1d6e39f984c787be3b2f237de12522386f987e27d67f

```

respone data

| parameter name   | whether necessary | type | description        | date range                                                |
| ----------- | -------- | -------- | -------------- | ------------------------------------------------------------ |
| user_id     | true     | long     | account id   |                                                              |
| volume      | true     | string   | volume |                                                              |
| deal_volume | true     | string   | excution volume  |                                                              |
| deal_money  | true     | string   | excution amount   |                                                              |
| fee         | true     | string   | transaction fees    |                                                              |
| id          | true     | string   | order id    |                                                              |
| price       | true     | string   | price of limit market |                                                              |
| status      | true     | String   | order status   | 1 ：new order,  2：order completed,  3 ：part completed,  4：canceled，6：Abnormal order |
| type        | true     | string   | order type       | buy-market， market buy, sell-market，market sell, buy-limit， limit buy, sell-limit， limit sell |
| source      | true     | string   | order source    | api                                                          |
| symbol      | true     | string   | trading pairs    | tchbtc,ltcbtc,ethbitcny ...                                  |
| ctime       | true     | string   | Order creation time |                                                              |
| mtime       | true     | string   | order completed time   |                                                              |

respone example：

```
{
    "code": "0",
    "msg": "suc",
    "data": {
        "symbol": "ethbtc",
        "fee": "0.00008001",
        "avg_price": "0.08001122",
        "source": 1,
        "type": "sell-limit",
        "mtime": 1526026018000,
        "volume": "1.000",
        "user_id": 10278,
        "price": "0.07936375",
        "ctime": 1526025991000,
        "deal_volume": "1.00000000",
        "id": 7383920,
        "deal_money": "0.08001122",
        "status": 2
    }
}
```