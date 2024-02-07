##### Common HTTP return error codes:
| Error Code| Description |
| ----------- | ----------- |
| **400**| missing a mandatory parameter |
| **402**| daily or monthly API calls limit exceeded |
| **403**| unauthorised access<br />*Possible reasons*:<ul><li>incorrect value of the API key (see the class constructor and parameter apiKey, privateKey)</li><li>access to the non-authorised method</li><li>wrong verification hash (wrong calculation or one of the calculation parameters incorrectly entered)</li><li>forbidden access to API</li><li>expiration of the API license</li></ul> |
