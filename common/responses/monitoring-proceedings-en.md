#### ProceedingResult
| Parameter | Popis |
| ----------- | ----------- |
| **DebtorsAddress** | List of addresses of debtors, bankrupt or defendants [`PersonAddress`](#PersonAddress). It depends on the type of event |
| **ProposersAddress** | List of proposers address [`PersonAddress`](#PersonAddress). It depends on the type of event |
| **AdministratorsAddress** | List of administrators or creditors addresses [`AdministratorAddress`](#AdministratorAddress) |
| **CourtsAddress** | ACourt address, if available [`CourtAddress`](#CourtAddress) |
| **ReferenceFileNumber** | Reference number of court file, type of lien, type of settlement, type of notification, type of submission |
| **Character** | Character of the decision |
| **Status** | Status of the proceeding |
| **PublishDate** | Date of event publishing (occasionaly it can be empty) |
| **Deadline** | Last deadline in the proceeding |
| **Type** |Type of the proceeding. <ul><li>LawSuit – court decision</li><li>PaymentOrder – payment order</li><li>Lien</li><li>Settlement</li><li>Notice</li><li>Bankruptcy</li><li>Restoration</li><li>Other</li><li>DistraintsAuthorizations – authorizations for distraint</li></ul> |
| **EndReason** | Reason of the end of a proceeding. It depends on the type of event |
| **EndStatus** | Final proceeding status |
| **Url** | URL for more information about the proceeding |
| **IssuedBy** | Information about a person that issued the proceeding [`IssuedPerson`](#IssuedPerson) |
| **PostedBy** | Information about a person that posted the proceeding |
| **FileIdentifierNumber** | list of File ID number if is available |