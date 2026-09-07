| Error code | Description |
| ----------- | ----------- |
| **400**| invalid request parameter value — the individual validations are listed with the parameters of each request above. The response body always contains the reason for the rejection. |
| **402**| in this group of requests **402 also means insufficient credit**, not only an exceeded daily or monthly API call limit (response ```Not enough credit```) |
| **502**| the distraints register (CRE — Centrálny register exekúcií) is temporarily unavailable or the query to it failed. **No credit is charged** in this case and the request can be repeated later. Applies to the requests that query CRE directly — *DistraintSearch* and *DistraintDetail*. |
