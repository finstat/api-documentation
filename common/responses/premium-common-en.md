##### Common detail parameters:
| Parameter | Description |
| ----------- | ----------- |
| **RegisterNumberText** | text description of the registration data - can be empty <ul><li>for a company in a form: Obchodný register XXXX súdu XXXXX, oddiel: xxx, vložka č.xxxx/x</li><li>for a entrepreneur (self employed): Okresný úrad XXXXX, Číslo živnostenského registra: xxx-xxxx</li></ul>|
| **Activity** | sector according to the FinStat categorisation – can be empty |
| **Created** | incorporation date in format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **Cancelled** | company dissolution date in a format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **SuspendedAsPerson** | flag if entrepreneur (self employed) is suspended (`true/false`) |
| **IcDphAdditional** | detailed information about VAT RN – [`IcDphAdditionalData`](#IcDphAdditionalData) – can be empty |
| **Warning** | flag if the company can be found in a list of debtors, bankrupties or liquidations (`true/false`) |
| **WarningUrl** | link to detailed information about a list of debtors, bankrupties or liquidation – can be empty |
| **PaymentOrderWarning** | flag if a payment order was issued for the company  (`true/false`) |
| **PaymentOrderUrl** | link to detailed information about company's payment orders – can be empty |
| **OrChange** | flag if any change in the Business register happened during the last 3 months (Unknown, Up, Down) |
| **OrChangeUrl** | link to detailed infomation with a list of fillings from the Business register |
| **SkNaceCode** | SK NACE code – can be empty |
| **SkNaceText** | SK NACE description – can be empty |
| **SkNaceDivision** | SK NACE division – can be empty |
| **SkNaceGroup** | SK NACE group – can be empty |
| **LegalFormCode** | legal form code (according Slovak statistical bureau) - can be empty |
| **LegalFormText** | legal form description - can be empty |
| **RpvsInsert** | flag if the company is listed in the Register of Public Sector Partners (RPVS) – can be empty |
| **RpvsUrl** | link to more information about people in the company on www.finstat.sk – can be empty |
| **ProfitActual** | earnings (last published year) – can be empty |
| **RevenueActual** | total amount of revenues (last published year) – can be empty |
| **JudgementIndicators** | list of court decision indicators [`JudgementIndicator`](#JudgementIndicator) |
| **JudgementFinstatLink** | link to more information about court decisions – can be empty |
| **SalesCategory** | category of company turnover – can be empty |
| **HasKaR** | flag of current bankruptcy or restructuring proceeding (`true/false`) |
| **KarUrl** | URL at more information about bankruptcy or restructuring proceeding – can be empty |
| **HasDebt** | flag of current debt, state or commercial recievables (`true/false`) |
| **DebtUrl** | URL at more information about current debt, state or commercial recievable – can be empty |
| **BankAccounts** | List of actual [`BankAccount`](#BankAccount) from Financial bureau – can be empty |
| **TaxReliabilityIndex** | Index of tax reliability - can be empty <br/>Values:<ul><li>highly reliable</li><li>reliable</li><li>less reliable</li><li>not rated</li></ul>|
| **SuspendedAsPersonUntil** | for a entrepreneur (self employed) only - the most closests date of suspendation |