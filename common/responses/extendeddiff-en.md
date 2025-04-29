##### Common diff parameters:
| Parameter | Description |
| ----------- | ----------- |
| **Ico**| ID number of a company (CIN) |
| **Dic**| Tax ID of a company (TIN) – can be empty |
| **IcDPH**| Vat Registration number of a company (VAT RN) – can be empty |
| **Name**| company nam – can be empty |
| **Street**|street of company's registered office – can be empty |
| **StreetNumber**| street number of company's registered office – can be empty |
| **ZipCode**|ZIP code of company's registered office  – can be empty |
| **City**| city of company's registered office  – can be empty |
| **District**| district  of company's registered office  – can be empty |
| **Region**| region  of company's registered office  – can be empty |
| **Url**| company link on  www.finstat.sk |
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
| **Phones** | list of telephone numbers `string` – can be empty |
| **Emails** | list of email addresses `string` – can be empty |
| **EmployeeCode** | code of the number of employees according to the Statistical bureau methodology – can be empty |
| **EmployeeText** | text expression the number of employees according to the Statistical bureau methodology – can be empty |
| **OwnershipTypeCode** | code of ownership type according to the Statistical bureau – can be empty |
| **OwnershipTypeText** | description of the ownership type – can be empty |
| **ActualYear** | year of published financial data – can be empty |
| **CreditScoreValue** | numeric expression of the credit score value – can be empty |
| **CreditScoreState** | text expression of the credit score value [`CreditScoreState`](#CreditScoreState) – can be empty |
| **ProfitActual** | earnings (last published year) – can be empty |
| **ProfitPrev** | earnings (previous year) – can be empty |
| **RevenueActual** | total amount of revenues (last published year) – can be empty |
| **RevenuePrev** | total amount of revenues (previous year) – can be empty |
| **ForeignResources** | foreign resources ratio (last published year) – can be empty |
| **GrossMargin** | gross margin (last published year) – can be empty |
| **ROA** | ROA of revenues (last published year) – can be empty |
| **Debts** | list of debts [`Debt`](#Debt) – can be empty |
| **PaymentOrders** | list of payment orders [`PaymentOrder`](#PaymentOrder) |
| **WarningKaR** | the day of last published filling about bankruptcy or restructuring (details can be found at WarningUrl) in format `RRRR-MM-DDTHH:MM:SS` – can be empty |
| **WarningLiquidation** | the last date of change in Liquidations (details can be found at WarningUrl) in format `RRRR-MM-DDTHH:MM:SS`– can be empty |