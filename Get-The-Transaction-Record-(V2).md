#### GET {Trading_Macro_v2}/order/match_results （query for the current trasaction , history transaction ）

Request parameters

| parameter subject | must or not | type   | describtion                         | defaults                      | ranges                                                       |
| ----------------- | ----------- | ------ | ----------------------------------- | ----------------------------- | ------------------------------------------------------------ |
| api_key           | true        | string | platform allocated api key          |                               |                                                              |
| symbol            | true        | string | trading pairs                       | btcbitcny, bchbtc, rcneth ... |                                                              |
| start-date        | false       | string | query for the start date yyyy-mm-dd | date format is yyyy-mm-dd     | maximum 7 days between the start date and the final log time |
| end-date          | false       | string | query for the end date              | date format is  yyyy-mm-dd    | maximum 7 days between the start date and the final log time |
| from              | false       | string | query for the start ID              | match ID                      | use with direct                                              |
| direct            | false       | string | query direction                     | default:next                  | prev ：forward，next：backwards                              |
| size              | false       | string | query the record amount             | default：50                   | query 50 record maximum at once                              |
| time              | true        | string | current timestamp                   |                               |                                                              |
request parameters：example (can not be used directly, need to replace your own parameters)

```
GET https://api.cointiger.com/api/v2/order/match_results?api_key=c9a97adf-7909-444a-bf9e-1471210c4770&sign=4d19bc9e7d84706dd45aa2e393675a7b775fe920751f769aeac75cf7b94c2b4bad4612534343437890e0ee2df769a227aa3f0d4d0db9305a67fb78ec314526bc&symbol=ethbtc&start-date=2018-05-11&end-date=2018-05-12&direct=next&size=10&time=1525515995127
```

response data

| parameter subject | must or not | type | describtionranges |                                                      |
| -------- | -------- | -------- | -------- | ------------------------------------------------------------ |
| id       | true     | long     | match ID  |                                                              |
| price    | true     | string   | commission price |                                                              |
| volume   | true     | string   | transaction amount   |                                                            |
| fee      | true     | string   | fees |                                                             |
| orderId  | true     | long     | order ID |                                                              |
| symbol   | true     | string   | trading pairs  | btcbitcny, bchbtc, eoseth ...                                |
| type     | true     | string   | entrust type | buy-market, sell-market, buy-limit, sell-limit |
| status   | true     | string   | order status | 1 ：new order, 2：compeletely deal,  3 ：partial deal,  4：revoked，6：abnormal order |
| mtime    | true     | string   | deal time |                                                              |
| source   | true     | string   | order source | api                                                          |

examples
```
{
  "status": "ok",
  "data": [{
		"id": 1084584,
		"price": 0.07231094,
		"volume": 1.000,
		"orderId": 5228948,
		"mtime": 1524823324000,
		"symbol": "ethbtc",
		"type": "buy-limit",
		"status": 2,
		"fee": 0.00100000,
		"source": "api"
	}...]
}
```