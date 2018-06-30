POST {Trading_Macro_v2}/order

request parameter

  name of parameter	whether necessary	type  	description                      	default	data range                 
  api_key          	true             	string	apikey distributed by platfrom   	       	                           
  symbol           	true             	string	trading pairs                    	       	tchbtc,ltcbtc,ethbitcny ...
  price            	true             	string	order price                      	       	                           
  volume           	true             	string	order amount                     	       	                           
  side             	true             	string	Business direction BUY  SELL     	       	                           
  type             	true             	string	1 ：limit trading，2：market trading	       	                           
  sign             	true             	string	signature                        	       	                           
  time             	true             	string	current timestamp                	       	                           

request parameter： for example （submit the parameter in "from-data" way）

    {
    	"symbol": "tchbtc",
    	"price": "10.1",
    	"volume": "100.1",
    	"side": "BUY",
    	"type": "1",
    	"sign": "d753734a6b94c051a0b9e4ca99a10bf2843b9bf41f74459790bb23de47dac5d06d339408e388adee614a84ad813a00f302104c88b062a685b0573b089e037c65",
    	"time": "1525515995127"
    }

response data

  parameter name	whether necessary	type  	description	data range
  order_id      	true             	string	ID         	          

response example

    {
    	"code": "0",
    	"msg": "suc",
    	"data": {
    		"order_id": 481
    	}
    }
