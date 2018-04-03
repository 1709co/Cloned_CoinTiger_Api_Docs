# [k line history data]()

#### [GET /market/history/kline ]()

NOTE

exchange $symbol$ for tch, btc eth btc 

------

request parameters

| parameters name | necessary or not | type  |       description    | defaults | ranges                                         |
| :------- | :------: | :------ | :---------------: | :----: | :------------------------------------------------- |
| api_key  |   true   | String  | api key distributed by the platform |        |                                                    |
| symbol   |   true   | String  |      trading pairs    |        | tchbtc, ethbtc,btcbitcny,eosbtc                    |
| period   |   true   | String  |      type of k line    |        | 1min,5min,15min,30min<br />60min,1day,1week,1month |
| size     |  false   | Integer |     obtain amount   |  150   | [1,2000]                                           |

------

response data

| parameters name | necessary or not |  type |                             description                        | ranges               |
| :------: | :------: | :----: | :----------------------------------------------------------: | --------------------------- |
|   code   |   true   | String |                         request processing status                   | 0 represent sucess and any others represent error |
|   msg    |   true   | String |                    specific error description or success decription                    |                             |
|    ch    |   true   | String | the channel which data belongs to.   format：market.$symbol$.kline.$period$<br /> |                             |

------

data 说明 data instruction: 

```
 "kline_data": [
            {
                "amount": 0.0004,//turnover
                "vol": 1,        //volume
                "high": 0.0004,  //highest price
                "low": 0.0004,   //lowest price
                "id": 1510416000,//the beginning of time scale
                "close": 0.0004, //open price
                "open": 0.0004   //close price
            }
        ]
```



------

请求响应示例: request response case

```
/* GET /api/market/history/kline?api_key=110311001&symbol=btcbitcny&period=1day&size=200 */

{
    "code": "0",
    "msg": "suc",
    "data": {
        "ch": "market.btcbitcny_kline.1day",
        "kline_data": [
            {
                "amount": 0.0004,
                "vol": 1,
                "high": 0.0004,
                "low": 0.0004,
                "id": 1510416000,
                "close": 0.0004,
                "open": 0.0004
            }
        ]
    }
}

/* GET /api/market/history/kline?api_key=110311001&symbol=btcbitcny&period=1day&size=200 */
{
    "code": "2",
    "msg": "you have exceeded  the limit times of calling api", 
    "ch": null,
    "ts": 0,
    "data": null
}

/* GET /api/market/history/kline?api_key=not-exist&symbol=btcbitcny&period=1day&size=200 */
{
    "code": "2",
    "msg": "api_key can not be air", 
    "data": null
}

/* GET /api/market/history/kline?api_key=110311001&symbol=not-exist&period=1day&size=200 */
{
    "code": "2",
    "msg": "symbol can not be air", 
    "data": null
}

/* GET /api/market/history/kline?api_key=110311001&symbol=btcbitcny&period=not-exist&size=200 */
{
    "code": "2",
    "msg": "period ca not be air", 
    "data": null
}

/*GET /api/market/history/kline?api_key=110311001&symbol=btcbitcny&period=1day&size=not-exist */
{
    "code": "2",
    "msg" : "the request parameters are illegal", //the ranges of parameters: [1,2000]
    "data": null
}

```

