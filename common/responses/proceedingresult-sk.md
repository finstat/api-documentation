#### ProceedingResult
| Parameter | Popis |
| ----------- | ----------- |
| **FileReference** | spisová značka |
| **CourtCode** | kód súdu |
| **StartDate** | dátum začatia podľa registra úpadcov|
| **EnterDate** | dátum vyhlásenie |
| **EnterReason** | dôvod začatia procesu podľa ORSR |
| **ExitDate** | dátum ukončenia konania |
| **ExitReason** | dôvod ukončenia konania |
| **Source** | zdroj <ul><li>BankruptcyRegister (Register úpadcov)</li><li>CommercialBulletin (Obchodný vestník)</li><li>CompaniesRegister (Obchodný register)</li></ul> |
| **Officers** | zoznam správcov [`Officer`](#Officer) |
| **Deadlines** | zoznam aktuálnych lehôt [`Deadline`](#Deadline) |
| **Status** | stav konania podľa Registra úpadcov |

#### BankruptResult
Štruktúra parametrov je totožná s [`ProceedingResult`](#ProceedingResult)

#### RestructuringResult
Štruktúra parametrov je totožná s [`ProceedingResult`](#ProceedingResult)