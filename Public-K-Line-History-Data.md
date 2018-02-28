# K Line History Data

**Request**

 

```
{
 "event":"req",
 "params":{
 	"channel":"market_$base$quote_kline_[1min/5min/15min/30min/60min/1day/1week/1month]",
	"cb_id":"customize",
	"since":"1506602880"
	  }
}
//When lacking, return the latest 300. Returns a maximum of 1 hour of data which is greater than since when there is a value. 
//Since has a strong self-correction, can not be earlier than the current 1 hour to take 59
```

 

**Return to Historical Data One Time**  

 

```
{
 "event_rep":"rep",
 "channel":"market_$base$quote_kline_[1min/5min/15min/30min/60min/1day/1week/1month]",
 "cb_id":"Return at the same way",
 "since":"1506602880",
       //When lacking, return the latest 300. Returns a maximum of 1 hour of data which is greater than since when there is a value. 
	   //Since has a strong self-correction, can not be earlier than the current 1 hour to take 59
 "ts":1506584998239,//Request time
 "data":[//300 pieces
 	{
	 "id":1506602880,//the numble of time scale starting
	 "amount":123.1221,//transaction amount
	 "vol":1212.12211,//transaction volume
	 "open":2233.22,//opening price
	 "close":1221.11,//closing price
	 "high":22322.22,//the highest price
	 "low":2321.22//the lowest price
	},
	{
	 "id":1506602880,//the numble of time scale starting
	 "amount":123.1221,//transaction amount
	 "vol":1212.12211,//transaction volume
	 "open":2233.22,//opening price
	 "close":1221.11,//closing price
	 "high":22322.22,//the highest price
	 "low":2321.22//the lowest price
	}
        ]
}

```

 

 