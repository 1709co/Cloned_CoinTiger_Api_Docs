# [market price lastest 24hours]()

#### [GET /market/detail ]()

NOTE

exchange $symbol$ for tch, btc eth btc 

------

request parameters:

| parameters name | necessary or not |  type |       description    | defaults | ranges                         |
| :------: | :------: | :----: | :---------------: | :----: | :-------------------------------- |
| api_key  |   true   | String | api key |        |                                   |
|  symbol  |   true   | String |      api key api key distributed by the platform      |        | tchbtc, ethbtc,btcbitcny,eosbtc.. |

------

response data:

| parameters name | necessary or not |  type  |                             descroption                           | ranges                  |
| :------: | :------: | :----: | :----------------------------------------------------------: | --------------------------- |
|   code   |   true   | String |                         request processing status                      | 0 represent sucess and any others represent error |
|   msg    |   true   | String |                    specific error description or success decription                |                             |
|    ch    |   true   | String | the channel which data belongs to.   format：market.$ symbol_depth.$type<br /> |                             |
|    ts    |   true   |  long  |                   the time of processing data unit:millisecond          |                             |

------

tick instruction:

```
"tick": {
            "amount": 8848738.84824509, // turnover
            "vol": 176.2158, // volume
            "high": 52892.62357326, // highest price
            "low": 49262.16, // lowest price
            "rose": -0.03721117, // change
            "close": 50281.60548325, // close price
            "open": 52743.50380325 // open price
        }
```

------

requset response case:

```
/* GET /api/market/detail?api_key=101311001&symbol=btcbitcny
{
    "code": "0",
    "msg": "suc",
    "data": {
        "ch": "market.btcbitcny.ticker",
        "trade_ticker_data": {
            "tick": {
                "amount": 7418370.49115073,
                "vol": 148.5636,
                "high": 52494.09797291,
                "low": 48645.1,
                "rose": -0.00656059,
                "close": 49375.30927674,
                "open": 51196.00406763
            },
            "ts": 1521747255985
        }
    }
}

/* GET /api/market/detail?api_key=101311001&symbol=btcbitcny
{
    "code": "2",
    "msg": "you have exceeded  the limit times of calling api", 
    "data": null
}

/* GET /api/market/detail?api_key=not-exist&symbol=btcbitcny
{
    "code": "2",
    "msg": "api_key can not be air",
    "data": null
}

/* GET /api/market/detail?api_key=101311001&symbol=not-exist
{
    "code": "2",
    "msg": "symbol can not be air",
    "data": null
}
```

