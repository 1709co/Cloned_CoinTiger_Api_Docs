

# Cancel Order

**/api/order  (DELETE)**

 **Request Parameter**

| Parameter | Types    | Description                  |
| --------- | -------- | ---------------------------- |
| api_key   | Required | assigned api key by platform |
| order_id  | Required | order ID                     |
| symbol    | Required | Market markup : eth / btc    |
| time      | Required | Time stamp                   |
| sign      | Required | Signature                    |

 

**Response**

 

| Field | Instance | Explanation |
| ----- | -------- | ----------- |
| code  | 0        |             |
| msg   | "suc"    | code>0 fail |
| data  |          |             |

 
