# Volume Depth

**Request**

 

```
{
 "event":"sub",
 "params":{
 	    "channel":"market_$base$quote_depth_step[0-2]",
 	    "cb_id":"customize",
 	    "asks":150,
 	    "bids":150
 	  }
}
```

 

**Return Subscription Status 1 Time**

 

```
{
 "event_rep":"subed",
 "channel":"market_$base$quote_depth_step[0-2]",
 "cb_id":"Return at the same way",
 "asks":150,
 "bids":150,
 "ts":1506584998239,
 "status":"ok"
}
```

 

**Continue To Return Subscribed News**

 

```
{
 "channel":"market_$base$quote_depth_step[0-2]",
            //$base$quote indicate btckrw etc.,Depth has 3 dimensions，0、1、2
 "ts":1506584998239,//request time
 "tick":{
	 "asks":[//sell
	 	 {22112.22,0.9332},
 		 {22112.21,0.2},
	        ],
	 "bids":[//buy
		 {22111.22,0.9332},
		 {22111.21,0.2},
	        ]
	}
}

```

 