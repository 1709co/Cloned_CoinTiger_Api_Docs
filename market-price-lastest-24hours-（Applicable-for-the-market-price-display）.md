GET https://www.cointiger.com/exchange/api/public/market/detail 



 Request parameters: no parameters：

---

The response data：

  parameter name	whether necessary	 type 	     description     	date range
    baseVolume  	      true       	String	       volume        	          
     high24hr   	      true       	String	     24 hr high      	          
    highestBid  	      true       	String	      best bid       	          
        id      	      true       	String	unique identification	          
       last     	      true       	String	     last price      	          
     low24hr    	      true       	String	      24 hr low      	          
    lowestAsk   	      true       	String	      best ask       	          
  percentChange 	      true       	String	       change        	          
   quoteVolume  	      true       	String	        total        	          

---

Request response example：

    /* GET https://www.cointiger.com/exchange/api/public/market/detail
    {
    	"TCHBTC": {
    		"baseVolume": "2698679.07986280",
    		"high24hr": "0.00000499",
    		"highestBid": "0.00000483",
    		"id": "1513853612681",
    		"last": "0.00000483",
    		"low24hr": "0.00000438",
    		"lowestAsk": "0.00000484",
    		"percentChange": "-0.00821355",
    		"quoteVolume": "12.45869455"
    	},
    	"ETCBTC": {
    		"baseVolume": "16423.52000053",
    		"high24hr": "0.00249400",
    		"highestBid": "0.00245800",
    		"id": "1513853461072",
    		"last": "0.00245800",
    		"low24hr": "0.00230841",
    		"lowestAsk": "0.00246100",
    		"percentChange": "0.04684838",
    		"quoteVolume": "31.81875637"
    	},
    	"ETHBTC": {
    		"baseVolume": "779.08061973",
    		"high24hr": "0.05016000",
    		"highestBid": "0.05009000",
    		"id": "1513853529349",
    		"last": "0.05009000",
    		"low24hr": "0.04745000",
    		"lowestAsk": "0.05016000",
    		"percentChange": "0.03921161",
    		"quoteVolume": "32.41927282"
    	},
    	"LTCBTC": {
    		"baseVolume": "7805.87000037",
    		"high24hr": "0.01900000",
    		"highestBid": "0.01883210",
    		"id": "1513853468581",
    		"last": "0.01885783",
    		"low24hr": "0.01840000",
    		"lowestAsk": "0.01885783",
    		"percentChange": "0.01114369",
    		"quoteVolume": "126.85474685"
    	},
    	"BCHBTC": {
    		"baseVolume": "801.59600000",
    		"high24hr": "0.26120000",
    		"highestBid": "0.21857000",
    		"id": "1513853451390",
    		"last": "0.21857000",
    		"low24hr": "0.18547516",
    		"lowestAsk": "0.22010000",
    		"percentChange": "-0.03713656",
    		"quoteVolume": "140.56031656"
    	}
    }
    
