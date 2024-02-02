# General info
## About API
### Main API functionality
**FinStat API** returns informations from  [FinStat.sk](https://www.finstat.sk).


> To use API, you need to have the unique API key – please, contact our sales department at ```info@finstat.sk```

> **Please note**, that all API versions can be extended with new parameters. We recommend you to use parsers that are not sensible to expansion of response structures.

> If you are interested in a higher API version or want to extend your current version with new parameters or data, please contact your trader or our sales department at ```info@finstat.sk```


### API Limits
Access to is limited by the number of requests.
- Daily limit: 4000 requests
- Monthly limit: 75000 requests

The number of maximal and currently spent daily limits can be found in a head of every response,<br />see example bellow:

``` http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: text/xml; charset=utf-8
Server: Microsoft-IIS/8.0
X-AspNetMvc-Version: 5.2

//Limits
Finstat-Daily-Limit-Current: 1
Finstat-Daily-Limit-Max: 4000
Finstat-Monthly-Limit-Current: 241
Finstat-Monthly-Limit-Max: 75000

X-AspNet-Version: 4.0.30319
X-Powered-By: ASP.NET
Date: Tue, 22 Sep 2015 13:57:38 GMT
Content-Length: 8437
```

> **Note:** Note: in the case of a limits exceeding, requests over limit are counted further. In the case of an unwanted exceeding of limits, for example due to some error in a code, it is possible to request their reset.

### Fair Use Policy
The recommended number of threads is 2. Although a higher amount is possible, there is a risk of automatic IP address blocking (in a case of a great load detection).

API is available througout the whole day, but you have to reckon with the fact that the server response during peak hours can be longer than its response during the night.
### JSON Support

To get response in JSON, use one of following switches:
- Send parameter ```json=true``` in URL request
<br />for example: ```https://www.finstat.sk/api/detail?json.true```
- End URL request with: ```.json```
<br />for example: ```https://www.finstat.sk/api/detail.json```

### Rules of API use
FinStat API was created for simple data transfet between FinStat servers and your application. To avoid security risks and excess API requests, do not implement your client  in a way that would makes your unique API keys visible to third parties or in a way that would make often unwanted requests.   

Inappropriate implementation is for example creation of javascript client that would call API directly from web browser. You would be at risk of exceeding your limit or abusing your keys.  

Always create a middleware on the call through which the entire communication will go on. In it you implement the correct computation of hashing strings and the correct API communication with your application. 

You can also use some of our example solutions. 

## General description of Hash function calculation
The purpose of the hash function is to check up on a customer request using hash function to which enter API key and one of the function parameters.  
> **Note:** All request definitions have specified parameters to use to generate hash values. 

### Hash function calculation 
1. Creation of a base value to calculate hash with hash salt, the base is `SomeSalt+{0}+{1}++{2}+ended`, where:
    - *{0}* – is a value of the API key 
    - *{1}* – is a value of the private API key
    - *{2}* – is a value of the function parameter (see **Hash parameter** in specification of every request)  
2. Hashing SHA256 is used to hash. In most cases, there is necessary to convert the base value to the field of byte values, with which SHA256 library can already work (every character from the base value is converted to its byte representation). 
3. The hash value calculation using the hash function SHA256 to the field of bytes. 
4. Conversion of the field of byte values to their text representation (every value in the field is converted to the two digits HEX format (0 => "00", 255 =>"FF"). 
5. Connection of all converted text values to a single value.

### Examples
#### C#
[](../common/csharp.md ':include')
#### PHP
[](../common/php.md ':include')
#### Java
[](../common/java.md ':include')
#### Visual Basic
[](../common/vbasic.md ':include')
#### Visual Basic for Applications
[](../common/vba.md ':include')