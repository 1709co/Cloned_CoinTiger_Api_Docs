# Get The Transaction Record

**/api/order/trade  (GET) : part transaction accomplish  of order**

 **Request Parameter**

| Parameter | Types    | Description                              |
| --------- | -------- | ---------------------------------------- |
| api_key   | Required | Assigned api key by platform             |
| offset    | Required | The number of  starting line , the mininum is 1 |
| limit     | Required | The number of getting                    |
| symbol    | Required | Market mark eg: ethbtc                   |
| time      | Required | Time stamp                               |
| sign      | Required | Signature                                |

 

**Response**

 

| Field | Instance                                 | Explanation                             |
| ----- | ---------------------------------------- | --------------------------------------- |
| code  | 0                                        |                                         |
| msg   | "suc"                                    | code>0 fail                             |
| data  | {"offset":1,"limit":100,"count":1000,"list":[]} | list content, see the following content |

 

```
{
	"volume": {
		"amount": "1.000",
		"icon": "",
		"title": "成交量"
	          },
	"price": {
		"amount": "0.04978883",
		"icon": "",
		"title": "委托价格"
	         },
	"created_at": 1513245134000,
	"deal_price": {
		"amount": 0.04978883000000000000000000000000,
		"icon": "",
		"title": "成交价格"
	              },
	"id": 138
}

```
