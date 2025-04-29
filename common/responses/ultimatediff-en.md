##### Common ultimatediff parameters:
| Parameter | Description |
| ----------- | ----------- |
| **Country**| country of company's registered office (if empty, then it is Slovak Republic) |
| **RpvsInsert** | flag if the company is listed in the Register of Public Sector Partners (RPVS) – can be empty |
| **RpvsUrl** | link to more information about people in the company on www.finstat.sk – can be empty |
| **JudgementIndicators** | list of court decision indicators [`JudgementIndicator`](#JudgementIndicator) |
| **JudgementFinstatLink** | link to more information about court decisions – can be empty |
| **KarUrl** | URL at more information about bankruptcy or restructuring proceeding – can be empty |
| **HasDebt** | flag of current debt, state or commercial recievables (`true/false`) |
| **DebtUrl** | URL at more information about current debt, state or commercial recievable – can be empty |
| **BasicCapital** | basic capital |
| **StateReceivables** | list of state recievables [`ReceivableDebt`](#ReceivableDebt) |
| **HasDisposal** | flag of active liquidation proceeding `true/false` |
| **DisposalUrl** | url to more information about liquidation proceeding |
| **SelfEmployed** | flag, if a subject is a entrepeneur (self - employed) `true/false` |
| **Offices** | list of offices [`Office`](#Office) – can be empty |
| **Subjects** | list of company subjects [`Subject`](#Subject) – can be empty |
| **ContactSources** | list of sources for contacts (parameters Emails, Phones) [`ContactSource`](#ContactSource) – can be empty |
| **StructuredName** | only available in entrepreneurs – it contains divided company name [`StructuredName`](#StructuredName) |
| **JudgementCounts** | list of numbers of court decisions [`JudgementCount`](#JudgementCount) – can be empty |
| **JudgementLastPublishedDate** | date of the last published court decision |
| **SalesCategory** | category of company turnover |
| **EmployeesNumber** | the exact number of employees - can be empty |
| **ORSection** | section in the Business Register |
| **ORInsertNo** |  insert in the Business Register |
| **Persons** |  people listed in the Business Register [`Person`](#Person)|
| **RpvsPerson** |  people listed in the Register of Public Sector Partners [`RpvsPerson`](#RpvsPerson)|
| **PaybackRange** | range of payback |
| **RegistrationCourt** | detailed information about registration court [`Court`](#Court)|
| **WebPages** | list of company web page `string` |
| **AddressHistory** | list of historical addresses [`HistoryAddress`](#HistoryAddress) |
| **StatutoryAction** | action of statutory - text description |
| **ProcurationAction** | action of procuration - text description |
| **Bankrupt** | information about bancrupcy [`BankruptResult`](#BankruptResult) |
| **Restructuring** | information about restructuralization [`RestructuringResult`](#RestructuringResult) |
| **Liquidation** | information about liquidation [`LiquidationResult`](#LiquidationResult) |
| **ORCancelled** | date of the company cancellation in the Business Register in a format `RRRR-MM-DDTHH:MM:SS` |
| **OtherProceeding** | information about other proceeding [`ProceedingResult`](#ProceedingResult) |
| **ORRemoved** | date of the company removal in the Business Register in a format `RRRR-MM-DDTHH:MM:SS` |
| **EmployeeYear** | year of last exact value of employees number |
| **ORLiquidationDate** | date of the company liquidation in the Business Register in a format `RRRR-MM-DDTHH:MM:SS` |
| **IncorporationDates** | list of all incorporation dates with source [`IncorporationDate`](#IncorporationDate) |
| **DissolutionDates** | list of all dissolution dates with source [`DissolutionDate`](#DissolutionDate) ||