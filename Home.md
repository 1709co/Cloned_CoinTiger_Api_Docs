 **support all trading pairs in CoinTiger** 

 **api.cointiger.com  domain name:api.cointiger.com**

 Tips: CoinTiger API please enter into the official website - personal account- API mangement to apply

  ## 一、API request address

  **Trading rest v2 api ** (new version) 

  ```
     Trading_Macro_v2 = https://api.cointiger.com/exchange/trading/api/v2
  ```

  **Trading rest api**  ( old version)

  ```
     Trading_Macro = https://api.cointiger.com/exchange/trading/api
  ```
  **Market rest api**  
  ```
     Market_Macro = https://api.cointiger.com/exchange/trading/api/market
  ```
  ##### Market  detail api  (Applicable to market display platform)

  ```
  	https://www.cointiger.com/exchange/api/public/market/detail (get)：
  ```

  **wss api**

  ```
  	wss://api.cointiger.com/exchange-market/ws
  ```

    注： Must carry parameters
     
    Language:zh_CN,en_US 

------

 


  ## 二、Public API Interface


  ```
 appropriate for coinTiger(The number of API calls is limited to 6 times per second)
  ```
  ### （1）Websocket API

  - [Request and subscription instructions](/cointiger/api-docs-en/wiki/Public-Request-And-Subscription-Instructions)
  - [K Line market](/cointiger/api-docs-en/wiki/Public-K-Line-Information) 
  - [last 24 hours market](/cointiger/api-docs-en/wiki/Public-The-Lastest-24-Hours-Price) 
  - [Real-time transaction information](/cointiger/api-docs-en/wiki/Public-Transaction-Information)
  - [deep handicap](/cointiger/api-docs-en/wiki/Public-Volume-Depth) 
  - [K line history data](/cointiger/api-docs-en/wiki/Public-K-Line-History-Data) 
  - [transaction history data](/cointiger/api-docs-en/wiki/Public-Transaction-History-Data) 

### （2)   REST API （v2-version）
 - [query the current time of the system](/cointiger/api-docs-en/wiki/query-the-current-time-of-the-system)
 - [query all crypto-currency supported by the cointiger platform](/cointiger/api-docs-en/wiki/currencys-（V2）)


  ###  （3） REST API

  - [last 24 hours market](/cointiger/api-docs-en/wiki/REST-market-price-lastest-24hours)
  - [deep handicap](/cointiger/api-docs-en/wiki/REST-volume-depth)
  - [K line history data](/cointiger/api-docs-en/wiki/REST-k-line-history-data)
  - [transaction history data](/cointiger/api-docs-en/wiki/REST-transaction-history-data)
  - [last 24 hours market position](/cointiger/api-docs-en/wiki/last-24-hours-market-position) (Applicable to market display platform)


------

### 三、（https） Trading API Interface （v2-version）

```
appropriate for coinTiger(The number of API calls is limited to 6 times per second)
```

- [create orders](/cointiger/api-docs-en/wiki/Create-Order-(V2)) 
- [Query the current order, history order](/cointiger/api-docs-en/wiki/query-for-the-current-commission,-history-commision-(V2))
- [Query current transaction, history transaction](/cointiger/api-docs-en/wiki/Get-The-Transaction-Record-(V2))
- [Query the transaction details of an order](/cointiger/api-docs-en/wiki/check-the-transaction-details-of-order-(V2)).
- [Query the details of an order](/cointiger/api-docs-en/wiki/query-order-specific-details-(V2))
- [Bulk cancel orders](/cointiger/api-docs-en/wiki/Bulk-cancel-orders（V2）)


### 四、（https）Trading API Interface

```
appropriate for coinTiger(The number of API calls is limited to 6 times per second)
```
- [Trading API signature rule](/cointiger/api-docs-en/wiki/Trading-API-Sign-Rules)
- [create orders](/cointiger/api-docs-en/wiki/Trading-Create-Order) 
- [get current orders](/cointiger/api-docs-en/wiki/Trading-Get-The-Current-Commission) 
- [cancel orders](/cointiger/api-docs-en/wiki/Trading-Cancel-Order) 
- [get history order](/cointiger/api-docs-en/wiki/Trading-Get-The-History-Commissioned) 
- [get transaction record](/cointiger/api-docs-en/wiki/Trading-Get-The-Transaction-Record)
- [get fund position](/cointiger/api-docs-en/wiki/Trading-Get-The-Fund-Information) 