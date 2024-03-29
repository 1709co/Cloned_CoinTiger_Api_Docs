﻿# [transaction history data]()

#### [GET /market/history/trade  ]()

NOTE

exchange $symbol$ for tch, btc eth btc 

------



request parameters:

| parameters name | necessary or not |  type   |  description  | defaults | ranges                          |
| :-------------- | ---------------- | :-----: | :-----------: | :------: | :------------------------------ |
| symbol          | true             | String  | trading pairs |          | tchbtc, ethbtc,btcbitcny,eosbtc |
| size            | false            | Integer | obtain amount |    1     | [1,2000]                        |

------

response data:

| parameters name | necessary or not |  type   |                         descroption                          | ranges                                          |
| :-------------: | :--------------: | :-----: | :----------------------------------------------------------: | ----------------------------------------------- |
|      code       |       true       | String  |                  request processing status                   | represent sucess and any others represent error |
|       msg       |       true       | String  |       specific error description or success decription       |                                                 |
|       ch        |       true       | String  | the channel which data belongs to.   format：market.$symbol$.trade.detail<br /> |                                                 |
|      size       |       true       | Integer |                        obtain amount                         |                                                 |
------

data instruction:

```
"trade_data": [
            {
                "id": 460760,               // trading id
                "side": "SELL",             // buy,sell buy and sell direction
                "price": 49375.30927674,    // unit price
                "vol": 0.0009,              // amount
                "amount": 44.43777834,      // total amount
                "ts": 1521747240000,        // time of processing data
                "ds": "2018-03-23 03:34:00" // time of formatting data
            }
        ]
```



------

request response case：


```
/* GET /api/market/history/trade?symbol=btcbitcny&size=200
{
    "code": "0",
    "msg": "suc",
    "data": {
        "trade_data": [
            {
                "id": 460760,
                "side": "SELL",
                "price": 49375.30927674,
                "vol": 0.0009,
                "amount": 44.43777834,
                "ts": 1521747240000,
                "ds": "2018-03-23 03:34:00"
            },
            {
                "id": 460759,
                "side": "SELL",
                "price": 49380.2519515,
                "vol": 0.001,
                "amount": 49.38025195,
                "ts": 1521747237000,
                "ds": "2018-03-23 03:33:57"
            }
        ],
        "size": 2,
        "ch": "market.btcbitcny_trade.detail"
    }
}

/* GET /api/market/history/trade?symbol=btcbitcny&size=200
{
    "code": "2",
    "msg": you have exceeded  the limit times of calling api",
    "data": null
}

/* GET /api/market/history/trade?symbol=not-exist&size=200
{
    "code": "2",
    "msg": "symbol can not be air",
    "data": null
}

/* GET /api/market/history/trade?symbol=not-exist&size=not-exist
{
    "code": "2",
    "msg": "the request parameters are illegal", //the ranges of parameters: [1,2000]
    "data": null
}

```
