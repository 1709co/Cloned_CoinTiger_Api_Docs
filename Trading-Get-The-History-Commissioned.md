

# Get The History Commissioned

**/api/order/history  (GET) : Including the transaction, revocation, cancellation part**

 **Request Parameter**

| Parameter | Types    | Description                              |
| --------- | -------- | ---------------------------------------- |
| api_key   | Required | assigned api key by platform             |
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
		"title": "volume"
	          },
	"age_price": {
		"amount": "0.00000000",
		"icon": "",
		"title": "Avg price"
	             },
	"side": "BUY",
	"price": {
		"amount": "0.04478883",
		"icon": "",
		"title": "price"
	         },
	"created_at": 1513415184838,
	"deal_volume": {
		"amount": "0.00000000",
		"icon": "",
		"title": "Deal volume"
	               },
	"id": 196,
	"label": {
		"go": "trade",
		"title": "Traded",
		"click": 1
	         },
	"side_msg": "Buy"
}

```
