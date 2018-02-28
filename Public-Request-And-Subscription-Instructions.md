# Request and subscription instructions



### 1. Address

```
wss://api.cointiger.com/exchange-market/ws
```

### 2. Data Compression

All data returned by the WebSocket API is GZIP-compressed, So client need to decompress after receiving the data

### 3. Heartbeat

WebSocket API supports bi-directional heartbeat, either Server or Client can initiate a `ping` message, then  the other party return `pong`message

WebSocket Server send heartbeats：

```
{"ping": 1519789122605}
```

WebSocket Client should return：

```
{"pong": 1519789122605}
```



### 4. Subscribed data(sub)

#### Subscribed data format

After successfully establishing the connection to the WebSocket API, the server sends data of the following format to subscribe data：

```
{
 "event":"sub",
 "params":{
 	    "channel":"xxx",// xxx corresponds to the Subscribed channel name
 	    "cb_id":"customize"
          }
}
```



### 5. Cancel Subscription(unsub)

#### format of canceling Subscription

After WebSocket Client subscribe data, client can cancel the subscription,.WebSocket Server will not send the topic data again after unsubscription, unsubscription format is as follows：

```
{
 "event":"unsub",
 "params":{
 	    "channel":"xxx",// xxx corresponds to the channel name that you want to cancel the subscription
 	    "cb_id":"customize"
 	  }
}
```