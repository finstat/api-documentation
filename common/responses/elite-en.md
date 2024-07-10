##### Common extended parameters:
| Parameter | Description |
| ----------- | ----------- |
| **Phones** | list of telephone numbers `string` – can be empty |
| **Emails** | list of email addresses `string` – can be empty |
| **EmployeeCode** | code of the number of employees according to the Statistical bureau methodology – can be empty |
| **EmployeeText** | text expression the number of employees according to the Statistical bureau methodology – can be empty |
| **OwnershipTypeCode** | code of ownership type according to the Statistical bureau – can be empty |
| **OwnershipTypeText** | description of the ownership type – can be empty |
| **ActualYear** | year of published financial data – can be empty |
| **CreditScoreValue** | numeric expression of the credit score value – can be empty |
| **CreditScoreState** | text expression of the credit score value [`CreditScoreState`](#CreditScoreState) – can be empty |
| **BasicCapital** | basic capital |
| **ProfitActual** | earnings (last published year) – can be empty |
| **ProfitPrev** | earnings (previous year) – can be empty |
| **RevenueActual** | total amount of revenues (last published year) – can be empty |
| **RevenuePrev** | total amount of revenues (previous year) – can be empty |
| **ForeignResources** | foreign resources ratio (last published year) – can be empty |
| **GrossMargin** | gross margin (last published year) – can be empty |
| **ROA** | ROA of revenues (last published year) – can be empty |
| **Debts** | list of debts [`Debt`](#Debt) – can be empty |
| **StateReceivables** | list of state recievables [`ReceivableDebt`](#ReceivableDebt) |
| **CommercialReceivables** | list of commercial recievables [`ReceivableDebt`](#ReceivableDebt) |
| **PaymentOrders** | list of payment orders [`PaymentOrder`](#PaymentOrder) |
| **WarningKaR** | the day of last published filling about bankruptcy or restructuring (details can be found at WarningUrl) in format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **WarningLiquidation** | the last date of change in Liquidations (details can be found at WarningUrl) in format `RRRR-MM-DDTHH:MM:SS`– can be empty |
| **HasDisposal** | flag of active liquidation proceeding `true/false` |
| **DisposalUrl** | url to more information about liquidation proceeding |
| **SelfEmployed** | flag, if a subject is a entrepeneur (self - employed) `true/false` |
| **Offices** | list of offices [`Office`](#Office) – can be empty |
| **Subjects** | list of company subjects [`Subject`](#Subject) – can be empty |
| **ContactSources** | list of sources for contacts (parameters Emails, Phones) [`ContactSource`](#ContactSource) – can be empty |
| **StructuredName** | only available in entrepreneurs – it contains divided company name [`StructuredName`](#StructuredName) |
| **JudgementFinstatLink** | url to more information about court decisions, if exists |
| **JudgementCounts** | list of numbers of court decisions [`JudgementCount`](#JudgementCount) – can be empty |
| **JudgementLastPublishedDate** | date of the last published court decision |
| **Ratios** | financial data for the last 4 years [`Ratio`](#Ratio) |
| **SalesCategory** | category of company turnover |
| **CreditScoreValueIndex05** | numeric expression of the Index05 credit score value – can be empty |
| **CreditScoreStateIndex05** | text expression of the Index05 credit score [`CreditScoreState`](#CreditScoreState) – can be empty |
| **DistraintsAuthorization** | information about distraints [`DistraintsAuthorizationInfo`](#DistraintsAuthorizationInfo) |
| **CreditScoreValueFinStatScore** | numeric expression of the FinStat credit score value in  percent - can be empty |
| **CreditScoreStateFinStatScore** | text expression of the FinStat credit score [`CreditScoreState`](#CreditScoreState) – can be empty |