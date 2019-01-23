## CoinTiger API document

CoinTiger provides stable and secure APIs. You can get the latest market data and trade via the APIs. Your trade-bot can run your algorithms to arbitrage or hedge. Now there are hundreds of algorithms in CoinTiger working safely.

#### API Request Address

| Request type | Request address                                              | foundation                 |
| ------------ | ------------------------------------------------------------ | -------------------------- |
| https        | Trading_Macro_v2 = https://api.cointiger.com/exchange/trading/api/v2 | new verision of trading    |
| https        | Trading_Macro = https://api.cointiger.com/exchange/trading   | history version of trading |
| https        | Market_Macro = https://api.cointiger.com/exchange/trading/api/market | market information         |
| websocket    | wss://api.cointiger.pro/exchange-market/ws                   |                            |

#### Create API key 

Please visit 【www.cointiger.com】-[Account] – [API control] – [create the new key] to create your own API Key.

#### **Request Process**

There are REST and Websocket two methods of Public Api Request; REST is the only method for Private Trading Api Request.

##### • Public Api

   REST：Require all trading pairs information , check system current time , all transaction information of all coins for last 24 hours, history transaction data of single trading pair, history K line data of single trading pair, ask/bid orders of single trading pair,and transaction data of single trading pair.

Websocket: Require transaction data of specific coins last 24 hours, data of ask/bid orders, real time data of K line, history data of K line, latest transaction data , and history transaction data.

##### • Private Trading Api

Private Trading Api was used to create/cancel bunch of orders, check current orders and history orders, transaction details ,order information and balance 

#### API Request limits

Both Public Api and Private Trading Api has a request limits.

REST

For every IP, API's access limit is 6times/second.

Websocket

For every IP, API's access limit is 6times/second.

 

#### API Request Step

##### • BaseURL

​     api.cointiger.com，Standby domain name:api.cointiger.pro 

##### • Sign Verification

​	REST：	

​           Rest require header must carry parameter, and meet RFC criterion, for example:

```
                  Language : zh_CN
                  User-Agent : Mozilla/5.0(Macintosh;U;IntelMacOSX10_6_8;en-
                               us)AppleWebKit/534.50(KHTML,likeGecko)Version/5.1Safari/534.50
                  Referer : https://api.cointiger.com
```

 Private Trading APi needs to do the sigh verification ,and Public Api do not.  
 [Private Trading API sign rules](/cointiger/api-docs-en/wiki/Trading-API-Sign-Rules) 

Websocket：

Request and subscription introduction 

API list

• [REST Api](/cointiger/api-docs-en/wiki/REST-Api-List)

• [Websocket Api](/cointiger/api-docs-en/wiki/Websocket-Api-List)

API community 

Welcome to CoinTiger API Telegram Group  <https://t.me/CoinTigerAPI>

 

API demo

1. Python : https://github.com/cointiger/CoinTiger_SDK_Python

2. Go : https://github.com/cointiger/CoinTiger_SDK_Golang

3. Java : https://github.com/cointiger/CoinTiger_SDK_JAVA

4. C# : https://github.com/cointiger/CoinTiger_SDK_CSharp 