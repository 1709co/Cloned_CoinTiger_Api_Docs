#### POST {Trading_Macro_v2}/order/batchcancel
`Request` parameters
| parameter subject | must or not | type | describtion | defaults | ranges       |
| ----------- | -------- | ------ | -------------- | ------ | -------------------- |
| orderIdList | true     | list   | cancel order ID |        | maximum50 order |
| time        | true     | string | timestamp   |        |                      |

request parameters example  (submit via form-data)
```
"api_key" : "c9a97adf-7909-444a-bf9e-1471310c4777"
"orderIdList"：{"btc":["5245365","5246402"],"ethbtc":["5245365","5246402"],...}
"time":1525515995127
"sign":"da5b9d029766f0430c111c668d67b23d45c60f55d16cb87498bda6175226cb0c8cadb1dbeb493317bd9740421ca0cbd01df218f6ae5b95decd9a410e9d317bb7"
```

response data:
| parameter subject | must or not | type | describtion | ranges |
| -------- | -------- | -------- | -------- | -------- |
| data     | false    | map      | cancel result |          |

example

```
{
	"code": "0",
	"msg": "suc",
	"data": {
		"success": [
			"1",
			"3"
		],
		"failed": [{
			"err-msg": "cancel failed",
			"order-id": "2",
			"err-code": "8"
		}]
	}
}
```