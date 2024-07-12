# AutoLogin API

## Autologin request
API Autologin creates URL address that automatically logs you into your account. Created 
address is available for 10 minutes and after its expiration you are redirected to login page. 

Response contains `string` element that is an autologin link for given url.

> **Requested URL**: ```https://www.finstat.sk/api/autologin```<br />
> **Hash parameter**: autologin

### Parameters
[](../../../common/parameters/autologin-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/autologin?url=https://finstat.sk/35757442&email=email@domena.tld&apikey=YourAPIKey&hash=cdab830acd61becad8aa9a7c501f68a9e8e03c37103e4ac52a4d0209d39781f5&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Example XML response
Examole XML response (for fiven url `https://finstat.sk/35757442`):

[](../../../common/examples/autologin.md ':include')