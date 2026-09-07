#### DistraintDetailResult
A single item of the **DistraintDetails** list in the [`DistraintDetailResults`](#DistraintDetailResults) response.
It contains all parameters of [`DistraintPreview`](#DistraintPreview) plus the detail data.

| Parameter | Description |
| ----------- | ----------- |
| **Code** | Code |
| **Debtors** | list of [`Debtor`](#Debtor) |
| **Pledgers** | list of [`Debtor`](#Debtor) |
| **TypeOfAuthorisation** | type of authorisation |
| **Created** | date when the request was created |
| **DetailId** | detail id needed for requesting detail |
| **DetailToken** | token for detail request |
| **StoredDetailId** | ID for stored detail in stored detail request |
| **Court** |  court |
| **DateOfAuthorisation** | date of authorisation |
| **CourtCode** | court code |
| **EnforcementDetails** | enforcement details  |
| **SumOutstanding** | total outstanding sum |
| **Currency** | currency |
| **Bailiff** | [`Bailiff`](#Bailiff) |