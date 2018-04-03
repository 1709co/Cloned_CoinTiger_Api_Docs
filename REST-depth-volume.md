# [depth volume]()

#### [GET /market/depth ]()

NOTE

exchange $symbol$ for tch, btc eth btc

------

request parameters:


| parameters name | necessary or not |  type   |       description      | defaults | ranges                        |
| :------- | :------: | :----: | :---------------: | :----: | :--------------------------------- |
| api_key  |   true   | String | api key api key api key distributed by the platform |        |                                    |
| symbol   |   true   | String |      trading pairs      |        | tchbtc, ethbtc,btcbitcny,eosbtc... |
| type     |   true   | String |    type of depth   |        | there are three dimensions in the depth. 0,1,2      |

------

response data:

| parameters name | necessary or not |  type  |                             decription                            |                     |
| :------: | :------: | :----: | :----------------------------------------------------------: | --------------------------- |
|   code   |   true   | String |                         request processing status                 | 0 represent sucess and any others represent error |
|   msg    |   true   | String |                    specific error description or success decription                 |                             |
|    ch    |   true   | String | the channel which data belongs to.   format：market.$ symbol$.depth.$type$ |                                     |

------

tick instriction:

```
 "tick": {
    "ts": the time of generating messages . unit: millisecond
    "buys": volume of buying. ,[price(transcation price), amount(volume)], price from high to low 
    "asks": volume of selling. ,[price(transcation price), amount(volume)], price from low to high
  }
```



------

response request  cas:

```
/* GET /api/market/depth?api_key=100310001&symbol=btcbitcny&type=step0 */
{
    "code": "0",
    "msg": "suc",
    "data": {
        "ch": "market.btcbitcny_depth.step0",
        "depth_data": {
            "tick": {
                "buys": [
                   ["49896.81", 0.0441],// [price, amount]
				  ["49936.23", 0.0021]
				  ...
				  // more data here
                ],
                "asks": [
                    ["49896.81", 0.0441],
				   ["49936.23", 0.0021]
				   ...
				   // more data here
                ]
            },
            "ts": 1521860775784
        }
    }
}

/* GET /api/market/depth?api_key=100310001&symbol=btcbitcny&type=step0 */
{
    "code": "2",
    "msg": "you have exceeded  the limit times of calling api",
    "data": null
}

/* GET /api/market/depth?api_key=not-exist&symbol=btcbitcny&type=step0 */
{
    "code": "2",
    "msg": "api_key can not be air",  
    "data": null
}

/* GET /api/market/depth?api_key=100310001&symbol=not-exist&type=step0 */
{
    "code": "2",
    "msg": "symbol can not be air", 
    "data": null
}

/* GET /api/market/depth?api_key=100310001&symbol=btcbitcny&type=not-exist */
{
    "code": "2",
    "msg": "type the request parameters are illegal", //  the ranges of 	parameters[step0,step1,step2] 
    "data": null
}

```

