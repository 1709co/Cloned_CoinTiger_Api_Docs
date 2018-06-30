#### GET {Trading_Macro_v2}/currencys  （check all the crypto-currency supported by CoinTiger）

request parameter 

non

Response Data

```
currency list
```

Response example

```
{
    "code": "0",
    "msg": "suc",
    "data": {
        "bitcny-partition": [
            {
                "baseCurrency": "btc",     // base currency 
                "quoteCurrency": "bitcny", // quote currency
                "pricePrecision": 2,       // digit of price accuracy (0 as :the unit)
                "amountPrecision": 4,      // digit of amount accuracy (0 as :the unit)
                "withdrawFeeMin": 0.0005,  // the minimum withdrawal fees.
                "withdrawFeeMax": 0.005,   // the maximum withdrawal fees.   
                "withdrawOneMin": 0.01,    // the minimum limit of withdrawal fees
                "withdrawOneMax": 10,      // the maximum limit of withdrawal fees
                "depthSelect": {           // depth selection setting
                    "step0": "0.01",       // Consolidation depth 0-2
                    "step1": "0.1",
                    "step2": "1"
                }
            },
            ...
        ]
    }
```