# Distraints search API
Information about executions directly in your information system

## RequestDistraintSearch request
Returns the list of previews to the execution based on the search criteria [`DistraintResult`](#DistraintResult).
Fee-based request.

> **Requested URL**: ```https://www.finstat.sk/api/requestdistraintsearch```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parameters

[](../../../common/parameters/distraint-search-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/requestdistraintsearch```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## RequestDistraintDetail request
Returns a list of previews to execution based on the searched ids [`DistraintDetail`](#DistraintDetail). 
Fee-based request

> **Requested URL**: ```https://www.finstat.sk/api/requestdistraintdetail```<br />
> **Hash parameter**: {token}{list ids connected without separators }

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |
| **ids**<br />*[mandatory]* | list of DetailId separated by commas |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/requestdistraintdetail```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## RequestDistraintResults request
The request returns the last historical request [`DistraintResult`](#DistraintResult) according search criteria

> **Requested URL**: ```https://www.finstat.sk/api/requestdistraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parameters

[](../../../common/parameters/distraint-search-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/requestdistraintresults```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## RequestDistraintResultsByToken request
The request returns the last historical request [`DistraintResult`](#DistraintResult) accorfing token.

> **Requested URL**: ```https://www.finstat.sk/api/requestdistraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/requestdistraintresultsbytoken```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## RequestDistraintStoredDetail request
The request returns the stored detail to the execution [`DistraintDetail`](#DistraintDetail).

> **Requested URL**: ```https://www.finstat.sk/api/requestdistraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **id**<br />*[mandatory]* | StoredDetailId |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/requestdistraintstoreddetail```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

# Response structures
[](../../../common/responses/distraint-result-en.md ':include')

[](../../../common/responses/distraintpreview-en.md ':include')

[](../../../common/responses/distraint-detail-en.md ':include')

[](../../../common/responses/debtor-en.md ':include')

[](../../../common/responses/bailiff-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/distraint-result.md ':include')

[](../../../common/examples/distraint-detail.md ':include')