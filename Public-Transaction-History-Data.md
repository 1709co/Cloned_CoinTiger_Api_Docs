# Transaction History Data

**Request**

 

```
{
 "event":"req",
 "params":{
        "channel":"market_$base$quote_trade_ticker",
        "cb_id":"customize",
        "top":200
	  }
}
```

 

**Directly Return The Transaction Information**

 

```
{
 "event_rep":"rep",
 "channel":"market_$base$quote_trade_ticker",
 "cb_id":"Return at the same way",
 "ts":1506584998239,
 "status":"ok",
 "top":200,//Maximum support200
 "data":[
	 {
	  "id":12121,//Transaction ID
	  "side":"buy",//Trading direction:buy,sell
	  "price":32.233,//Unit price
	  "vol":232,//volume
	  "amount":323,//amount
	  "ts":1506584998239//Data generation time
	 },
	 {
	  "id":12120,//Transaction ID
	  "side":"buy",//Trading direction:buy,sell
	  "price":32.233,//Unit price
	  "vol":232,//volume
	  "amount":323,//amount
	  "ts":1506584998239,//Data generation time
	  "ds":'2017-09-10 23:12:21'
	 }
	]
}

```

 

 