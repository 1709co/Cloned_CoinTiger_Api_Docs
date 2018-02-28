# K Line Information

**Request**

 

```
{  
 "event":"sub",
 "params"：{
    "channel":"market_$base$quote_kline_[1min/5min/15min/30min/60min/1day/1week/1month]",
    "cb_id":"Customize"
           }
}
```

 

**Return Subscription Status 1 Time**

 

```
{
  "event_rep":"subed",
  "channel":"market_$base$quote_kline_[1min/5min/15min/30min/60min/1day/1week/1month]",
  "cb_id":"Return at the same way",
  "ts":1506584998239,
  "status":"ok"
}
```

 

**Continue To Return Subscribed News**

 

```
{
  "channel":"market_$base$quote_kline_[1min/5min/15min/30min/60min/1day/1week/1month]",
	//Subscribed trading pairs price in the market $base$quote indicate btckrw etc.
   "ts":1506584998239,//request time
   "tick":{
 	 "id":1506602880,//the numble of time scale starting
         "amount":123.1221,//Transaction amount
 	 "vol":1212.12211,//Trading volume
 	 "open":2233.22,//Opening price
 	 "close":1221.11,//Closing price
 	 "high":22322.22,//The highest price
 	 "low":2321.22//The lowest price
 		}
}
```

 