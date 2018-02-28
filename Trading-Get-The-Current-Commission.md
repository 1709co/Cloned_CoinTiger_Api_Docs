# Get The Current Commission

**/api/order/new  (GET) : include completed and not completed**

 **Request Parameter**

| Parameter | Types    | Description                              |
| --------- | -------- | ---------------------------------------- |
| api_key   | Required | assigned api key by platform             |
| offset    | Required | The number of  starting line , the minimum is 1 |
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
		"title": "The quantity in the commission"
	          },
	"side": "BUY",
	"price": {
		"amount": "0.04478883",
		"icon": "",
		"title": "Commissioned price"
	         },
	"created_at": 1513415184838,
	"id": 196,
	"label": {
		"title": "cancel order",
		"click": 1
	         },
	"remain_volume": {
		"amount": "1.00000000",
		"icon": "",
		"title": "Not completed"
	        },
	"side_msg": "buy"
}

```
