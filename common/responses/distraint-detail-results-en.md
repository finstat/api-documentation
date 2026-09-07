#### DistraintDetailResults
Wrapper object returned by the *DistraintDetail* and *DistraintStoredDetail* requests.
Even when the request resolves to a single detail, the response is always this wrapper
containing a list.

| Parameter | Description |
| ----------- | ----------- |
| **DistraintDetails** | list of [`DistraintDetailResult`](#DistraintDetailResult); when nothing was found an empty element ```<DistraintDetails />``` is returned |
