##### Additional parameters:
| Parameter | Description |
| ----------- | ----------- |
| **VATNumber** | Vat Registration number of a company (VAT RN) – can be empty  |
| **TaxPayer** | type of VAT payer  – can be empty <ul><li>Platce</li><li>IdentifikovanaOsoba< li><li>OsobaIdentifikovanaKDani</li></ul>|
| **LegalFormCode** | legal form code (according Slovak statistical bureau) - can be empty |
| **OwnershipTypeCode** |  ownership type code  - can be empty |
| **BankAccounts** | list of actual [`BankAccount`](#BankAccount) from bureau – can be empty |
| **Unreliability** | flag if subject is unreliabile payer or person|
| **RegisterNumberText** | text description of the registration data - can be empty <ul><li>Obchodný register XXXX súdu XXXXX, oddiel: xxx, vložka č.xxxx/x</li></ul>|
| **TradeLicensingOffice** | trade office info for self employed subject - can be empty <ul><li>XXXXX</li></ul>|
| **ActualYear**| year of published financial data – can be empty |
| **SalesActual**| earnings (last published year) – can be empty |
| **ProfitActual**| total sum of sales (last published year) – can be empty |
| **Sales**| flag of sales movement in comparasion to previous published year. Enum type (`Unknown, Up, Down`) |
| **Profit**| flag of profit movement in comparasion to previous published year. Enum type (`Unknown, Up, Down, Loss`) |