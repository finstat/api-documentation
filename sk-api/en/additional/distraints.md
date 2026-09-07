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

> **Price:** charged as **1 query** (one price unit according to your licence).

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

[](../../../common/http/errorcodes-en-distraint.md ':include')

## DistraintDetail request
Returns the distraint details based on the searched ids.
The response is the [`DistraintDetailResults`](#DistraintDetailResults) wrapper containing the
**DistraintDetails** list, whose items are of the [`DistraintDetailResult`](#DistraintDetailResult)
type — even when a single id is requested.
Fee-based request.

> **Requested URL**: ```https://www.finstat.sk/api/distraintdetail```<br />
> **Hash parameter**: {token}{list ids connected without separators }

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |
| **ids**<br />*[mandatory]* | list of DetailId separated by commas |

##### Parameter validations
Violating any of them returns **HTTP 400** with the reason in the response body:

| Validation | Response body |
| ----------- | ----------- |
| `token` must be filled in | ```'token' parameter not specified!``` |
| `ids` must contain at least one **numeric** id; a non-numeric value in the list invalidates the whole parameter | ```'ids' parameter not valid!``` |
| after duplicates are removed the `ids` list may contain **at most 200** identifiers | ```'ids' parameter maximum size of 200 identifiers exceeded!``` |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintdetail```

> **Price:** this request is **not charged as a single query** — the **number of unique identifiers**
in the `ids` parameter is charged. A request with 10 distinct ids is therefore charged as 10 queries.
Duplicate ids are removed before charging. When there is not enough credit for the required amount,
**402** is returned and the register is not queried at all.

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

[](../../../common/http/errorcodes-en-distraint.md ':include')

## DistraintResults request
The request returns the last historical request [`DistraintResult`](#DistraintResult) according search criteria

> **Requested URL**: ```https://www.finstat.sk/api/distraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parameters

[](../../../common/parameters/distraint-search-en.md ':include')

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintresults```

> **Price:** this request is not charged against your credit, it reads an already paid historical request.
It still counts towards the daily and monthly API call limits.

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

[](../../../common/http/errorcodes-en-distraint.md ':include')

## DistraintResultsByToken request
The request returns the last historical request [`DistraintResult`](#DistraintResult) accorfing token.

> **Requested URL**: ```https://www.finstat.sk/api/distraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **token**<br />*[mandatory]* | DetailToken |

An empty `token` returns **HTTP 400** with the body ```'token' parameter not specified!```.

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintresultsbytoken```

> **Price:** this request is not charged against your credit, it reads an already paid historical request.
It still counts towards the daily and monthly API call limits.

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

[](../../../common/http/errorcodes-en-distraint.md ':include')

## DistraintStoredDetail request
The request returns an already stored distraint detail.
The response is the [`DistraintDetailResults`](#DistraintDetailResults) wrapper containing the
**DistraintDetails** list, whose items are of the [`DistraintDetailResult`](#DistraintDetailResult)
type. Since a single `id` is requested, the list contains at most one item; when no detail was
found, an empty element ```<DistraintDetails />``` is returned.

> **Requested URL**: ```https://www.finstat.sk/api/distraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **id**<br />*[mandatory]* | StoredDetailId |

An empty `id` returns **HTTP 400** with the body ```'id' parameter not specified!```.

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/distraintstoreddetail```

> **Price:** this request is not charged against your credit, it reads an already paid detail.
It still counts towards the daily and monthly API call limits.

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

[](../../../common/http/errorcodes-en-distraint.md ':include')

# Response structures
[](../../../common/responses/distraint-result-en.md ':include')

[](../../../common/responses/distraintpreview-en.md ':include')

[](../../../common/responses/distraint-detail-results-en.md ':include')

[](../../../common/responses/distraint-detail-en.md ':include')

[](../../../common/responses/debtor-en.md ':include')

[](../../../common/responses/bailiff-en.md ':include')

> **Note:** order of parameters can be different from list above

# Example XML response
[](../../../common/examples/distraint-result.md ':include')

[](../../../common/examples/distraint-detail.md ':include')