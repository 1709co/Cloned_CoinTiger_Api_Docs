# Create Order

**/api/order  (POST)**

 **Request Parameter**

| Parameter        | Types    | Description                              |
| ---------------- | -------- | ---------------------------------------- |
| api_key          | Required | assigned api key by platform             |
| side             | Required | Trading direction：BUY、SELL               |
| type             | Required | Pending order type<br/>1: limit commission<br/>2: market commission |
| volume           | Required | Purchase amount  (Polysemy, Multiplex Fields) <br/>type=1:indicate  the number of transactions<br/>type=2:buy indicate total price, sell indicate  the total number<br/>Trading restrictions user / me-user information |
| capital_password | Required | Funding password, based on user password type |
| price            | Required | Unit Price: type = 2: This parameter is not required |
| symbol           | Required | Market markup, 202201: eth / btc         |
| time             | Required | Time stamp                               |
| sign             | Required | Signature                                |

 

**Response**

 

| Field | Instance           | Explanation                       |
| ----- | ------------------ | --------------------------------- |
| code  | 0                  |                                   |
| msg   | "suc"              | code>0 fail                       |
| data  | {"order_id":34343} | success, return to transaction ID |

 

 **Virtual coin number   	 xxx-btc(xxx201)**



| btc  |        |
| :--: | :----: |
| eth  | ethbtc |
| ltc  | ltcbtc |
| bcc  | bccbtc |
| etc  | etcbtc |
| tch  | tchbtc |
