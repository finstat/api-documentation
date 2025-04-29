#### ReceivableDebt
| Parameter | Description |
| ----------- | ----------- |
| **Source** | recievables manager |
| **Value** | value of recievable |
| **ValidFrom** | date of a debt detection in format `RRRR-MM-DDTHH:MM:SS` |

#### Office
| Parameter | Description |
| ----------- | ----------- |
| **Street** | street |
| **StreetNumber** | street number |
| **City** | town/city |
| **ZipCode** | ZIP code |
| **District** | district |
| **Region** | region |
| **Country** | country/state |
| **Subjects** | list of company's subjects `string` |
| **Type** | type of the address |

#### JudgementCount
| Parameter | Description |
| ----------- | ----------- |
| **Name** | acting side of law suit <ul><li>Defendant</li><li>Plaintiff</li><li>Attorney</li></ul> |
| **Value** | number of court decisions for acting side |

#### Person
| Parameter | Description |
| ----------- | ----------- |
| **FullName** | full name or company name |
| **Street** | street name |
| **StreetNumber** | street number |
| **City** | city/town |
| **District** | district |
| **Region** | region |
| **Country** | country/state |
| **DepositAmount** | amount of the deposit |
| **PaybackRange** | range of payback |
| **DetectedFrom** | date of detection of the function start in format `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | date of detection of the function end in format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **Functions** | list of functions [`FunctionAssigment`](#FunctionAssigment) |
| **StructuredName** | name in of a person in a structured form [`StructuredName`](#StructuredName) |
| **Ico** | company ID number - can be empty |

#### RpvsPerson
| Parameter | Description |
| ----------- | ----------- |
| **FullName** | full name or company name |
| **Street** | street name |
| **StreetNumber** | street number |
| **City** | city/town |
| **District** | district |
| **Region** | region |
| **Country** | country/state |
| **Ico** | company ID number - can be empty |
| **BirthDate** | date of birth |
| **DetectedFrom** | date of detection of the function start in format `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | date of detection of the function end in format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **Functions** | list of functions [`FunctionAssigment`](#FunctionAssigment) |
| **StructuredName** | name in of a person in a structured form [`StructuredName`](#StructuredName) |

#### StructuredName
| Parameter | Description |
| ----------- | ----------- |
| **Prefix** | list of degrees  `string`|
| **Name** | name (max 2 items) `string` |
| **Suffix** | list of titles behind the name `string` |
| **Name** | all the other words behind the name `string` |

#### Court
| Parameter | Description |
| ----------- | ----------- |
| **Name** | name, if available |
| **Street** | street, if available |
| **StreetNumber** | street number, if available |
| **ZipCode** | ZIP code, if available |
| **City** | city or town, if available |
| **District** | district, if available |
| **Region** | region, if available |
| **Country** | country, if available |

#### HistoryAddress
| Parameter | Description |
| ----------- | ----------- |
| **Street** | street |
| **StreetNumber** | street number |
| **City** | mesto |
| **ZipCode** | ZIP code |
| **District** | district |
| **Region** | region |
| **Country** | country/sate |
| **ValidFrom** | date from when we dectect it as a valid address in format `RRRR-MM-DDTHH:MM:SS` |
| **ValidTo** | end date from when we dectect it as a valid address  in format `RRRR-MM-DDTHH:MM:SS` |


#### ProceedingResult
| Parameter | Description |
| ----------- | ----------- |
| **FileReference** | file reference number |
| **CourtCode** | court code |
| **StartDate** | the date of starting of bankruptcy proceeding |
| **EnterDate** | entry date |
| **EnterReason** |entry reason |
| **ExitDate** | exit date |
| **ExitReason** | exit reasons |
| **Source** | source <ul><li>BankruptcyRegister</li><li>CommercialBulletin</li><li>CompaniesRegister</li></ul> |
| **Officer** | officer [`Person`](#Person) |
| **Deadlines** | deadlines in proceeding [`Deadline`](#Deadline) |
| **Status** | proceeding state |
| **ProposalDate** |  date of proposalin format `RRRR-MM-DDTHH:MM:SS`|
| **CourtPublishingDate** |  date of court publishing in format `RRRR-MM-DDTHH:MM:SS`|

#### BankruptResult
Structure of parameters is the same as in [`ProceedingResult`](#ProceedingResult)

#### RestructuringResult
Structure of parameters is the same as in [`ProceedingResult`](#ProceedingResult)

#### LiquidationResult
| Parameter | Description |
| ----------- | ----------- |
| **EnterDate** | entry date |
| **EnterReason** | entry reason |
| **ExitDate** | exit date |
| **Source** | source <ul><li>CompaniesRegister</li></ul> |
| **Officer** | officer [`Person`](#Person) |
| **Deadline** | deadline description |
| **LiquidatorProcedure** | proceeding |
| **CancelReason** | readon of cancellation  |
| **DeleteReason** |  reason of deletion |

#### Deadline
| Parameter | Description |
| ----------- | ----------- |
| **Type** | description |
| **Date** | date in format `RRRR-MM-DDTHH:MM:SS` |

#### IncorporationDate
| Parameter | Description |
| ----------- | ----------- |
| **Date** | incorporation date in format `RRRR-MM-DDTHH:MM:SS` |
| **Source** | source |

#### DissolutionDate
| Parameter | Description |
| ----------- | ----------- |
| **Date** | dissolution date in format `RRRR-MM-DDTHH:MM:SS` |
| **Source** | source |