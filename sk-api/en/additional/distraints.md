# Distraints search API
Information about executions directly in your information system

## DistraintSearch request
Returns the list of previews to the execution based on the search criteria [`DistraintResult`](#DistraintResult).
Fee-based request.

> **Requested URL**: ```https://www.finstat.sk/api/distraintsearch```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parameters

[](../../../common/parameters/distraint-search-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintsearch```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## DistraintDetail request
Returns a list of previews to execution based on the searched ids [`DistraintDetail`](#DistraintDetail). 
Fee-based request

> **Requested URL**: ```https://www.finstat.sk/api/distraintdetail```<br />
> **Hash parameter**: {token}{list ids connected without separators }

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |
| **ids**<br />*[mandatory]* | list of DetailId separated by commas |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintdetail```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## DistraintResults request
The request returns the last historical request [`DistraintResult`](#DistraintResult) according search criteria

> **Requested URL**: ```https://www.finstat.sk/api/distraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parameters

[](../../../common/parameters/distraint-search-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintresults```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## DistraintResultsByToken request
The request returns the last historical request [`DistraintResult`](#DistraintResult) accorfing token.

> **Requested URL**: ```https://www.finstat.sk/api/distraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintresultsbytoken```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## DistraintStoredDetail request
The request returns the stored detail to the execution [`DistraintDetail`](#DistraintDetail).

> **Requested URL**: ```https://www.finstat.sk/api/distraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **id**<br />*[mandatory]* | StoredDetailId |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintstoreddetail```

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