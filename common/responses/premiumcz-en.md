##### Additional parameters:
| Parameter | Description |
| ----------- | ----------- |
| **VATNumber** | Vat Registration number of a company (VAT RN) – can be empty  |
| **TaxPayer** | flag if subject is a tax payer (`true/false`)|
| **LegalFormCode** | legal form code (according Slovak statistical bureau) - can be empty |
| **OwnershipTypeCode** |  ownership type code  - can be empty |
| **BankAccounts** | List of actual [`BankAccount`](#BankAccount) from bureau – can be empty |
| **Unreliability** | flag if subject is unreliabile payer or person|
| **RegisterNumberText** | text description of the registration data - can be empty <ul><li>for a company in a form : Zapísaná na Okr. súde XXXXX, odd. Sro, vl.č.xxxx/L</li><li>for a entrepreneur (self employed): Číslo živn.registra: xxx-xxxx, okresný úrad XXXXX </li></ul>|
| **ActualYear**| year of published financial data – can be empty|
| **SalesActual**| Earnings (last published year) – can be empty |
| **ProfitActual**| Total sum of sales (last published year) – can be empty |
| **Sales**| flag of sales movement in comparasion to previous published year  (Unknown, Up, Down) |
| **Profit**| flag of profit movement in comparasion to previous published year (Unknown, Up, Down, Loss) |