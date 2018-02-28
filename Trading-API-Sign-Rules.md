# Trading API Sign Rules

#### 1. General Rules	

1. &nbsp;&nbsp; All APIs, except for the public api, need to carry the parameter sign

2. &nbsp;&nbsp; All APIs need to carry  time parameters (timestamp), and sign (sign, whitelist except api)

3. &nbsp;&nbsp;Sign signature verification rules 

    1)    POST request, SRV combines and gets all the parameters of post t. Please do not set the same key. When POST, time, token  and  sign are put into get parameter.

    2)    Ask the user to save the apikey and apisecret assigned to the user as the encryption key

    3)    the rules of creating sign：sign=HMAC-SHA512(key1+value1+key2+value2+secret)

    4)    The keys of all parameters are arranged in ascending alphabetical order. 

4. &nbsp;&nbsp; The return value structure of the outer fixed {"code": 0, "msg": "suc", "data": ""}

    1)    code: 0 for success, greater than 0, you can refer to msg return

    2)    msg: return error message

    3)    data: There are three return values, "", {}, [], need to be resolved according to the interface return value


#### 2. Universal Return Code

Note: 100001-110000, System error reserved segment

100001:   System is abnormal

100002：System upgrade, service suspension

100003：Request is illegal