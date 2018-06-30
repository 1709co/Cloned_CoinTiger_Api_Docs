#### GET {Trading_Macro_v2}/order/make_detail （check the transaction details of order）

request parameter:

| name of parameter | whether necessary | type  | desceiption          | default | data range                    |
| -------- | -------- | ------ | ----------------- | ------ | ----------------------------- |
| api_key  | true     | string | api key  api key distributed by the platform |        |                               |
| symbol   | true     | string | trading pairs     |        | btcbitcny, bchbtc, eoseth ... |
| order_id | true     | string | order ID     |        |                               |
| sign     | true     | string | signature         |        |                               |
| time     | true     | string | current timestamps       |        |                               |

request parameter：for example（ can not use directly and need to replace bu your own parameter）

```
GET https://api.cointiger.com/exchange/trading/api/v2/order/make_detail?api_key=c9a97adf-7909-444a-bf9e-1471210c4782&time=1525524649346&order_id=7161220&symbol=ethbtc&sign=d753734a6b94c051a0b9e4ca99a10bf2843b9bf41f74459790bb23de47dac5d06d339408e388adee614a84ad813a00f302104c88b062a685b0573b089e037c65

```

response data

| name of parameter | whether necessary | type | desceiption                                     | data range                                            |
| ----------- | -------- | -------- | ----------------------------------------------- | ------------------------------------------------------------ |
| id          | true     | long     | ID                                  |                                                              |
| volume      | true     | string   | trading volume                            |                                                              |
| price       | true     | string   | price                         |                                                              |
| symbol      | true     | string   | trading pairs                             |                                                              |
| type        | true     | string   | type of order                      | buy-market, sell-market, buy-limit, sell-limit |
| source      | true     | string   | resource of order                            | api                                                          |
| orderId     | true     | string   | order ID                    |                                                              |
| bid_user_id | true     | string   | buyer ID If the order is to bid, the field is not empty |                                                              |
| ask_user_id | true     | string   | seller ID If the order is to askl, the field is not empty |                                                              |
| buy_fee     | true     | string   | transaction fees                           |                                                              |
| created     | true     | string   | turnover time                           |                                                              |

Response example

```
{
	"code": "0",
	"msg": "suc",
	"data": [{
            "volume": "0.037",
            "symbol": "ethbtc",
            "ask_user_id": 10278,
            "orderId": 7383871,
            "price": "0.08024551",
            "created": 1526025997000,
            "id": 1152950,
            "source": 1,
            "type": "sell-limit",
            "sell_fee": "0.00000296"
        },
        ...]
}
```