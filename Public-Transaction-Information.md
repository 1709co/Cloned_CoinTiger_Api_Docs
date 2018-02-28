# Transaction Information

**Request**

 

```
{
 "event":"sub",
 "params":{
 	    "channel":"market_$base$quote_trade_ticker",
 	    "cb_id":"customize"
 	  }
}
```

 

**Return Subscription Status 1 Time**

 

```
{
  "event_rep":"subed",
  "channel":"market_$base$quote_trade_ticker",
  "cb_id":"Return at the same way",
  "ts":1506584998239,
  "status":"ok"
}
```

 

**Continue To Return Subscribed News**

 

```
{
 "channel":"market_$base$quote_trade_ticker",
 		//Subscribed trading pairs price in the market $base$quote indicate btckrw etc.
 "ts":1506584998239,//request time
 "tick":{
	"id":12121,//Maximum transaction ID in the data
	"ts":1506584998239,//Maximum time in the data
	"data":[
		{
		   "id":12121,//Transaction ID
		   "side":"buy",//Trading direction:buy,sell
		   "price":32.233,//Unit price
		   "vol":232,//Volume
		   "amount":323,//Amount
		   "ts":1506584998239,//Data generation time
		   "ds":'2017-09-10 23:12:21'
		},
		{
		   "id":12120,//Transaction ID
		   "side":"buy",//Trading direction:buy,sell
		   "price":32.233,//Unit price
		   "vol":232,//Volume
		   "amount":323,//Amount
		   "ts":1506584998239,//Data generation time
		   "ds":'2017-09-10 23:12:21'
		}
	     ]
        }
}

```

 