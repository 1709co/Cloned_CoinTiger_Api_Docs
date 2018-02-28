# Get The Fund Information

**/api/user/balance  (GET)**

 **Request Parameter**

| Parameter | Types                                    | Description                  |
| --------- | ---------------------------------------- | ---------------------------- |
| api_key   | Required                                 | Assigned api key by platform |
| coin      | Optional, if not return to all currencies | btc,eth  needs lowercas      |
| time      | Required                                 | Time stamp                   |
| sign      | Required                                 | Signature                    |

 

**Response**

 

| Field | Instance                  | Explanation                              |
| ----- | ------------------------- | ---------------------------------------- |
| code  | 0                         |                                          |
| msg   | "suc"                     | code>0 fail                              |
| data  | the instance is as follow | normal：Available funds<br/>lock：Freeze funds |


```
{
  "code": "0",
  "msg": "suc",
  "data": [
    {
      "normal": "1813.01144179",
      "lock": "1325.42036785",
      "coin": "btc"
    },
    {
      "normal": "9551.96692244",
      "lock": "547.06506717",
      "coin": "eth"
    }
  ]
}

```
