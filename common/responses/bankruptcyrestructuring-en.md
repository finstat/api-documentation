#### BankruptcyRestructuring
| Parameter | Description |
| ----------- | ----------- |
| **Debtors** | list of debtors of type [`PersonAddress`](#PersonAddress) |
| **FileReference** | file reference number |
| **FirstRecordDate** | date of the first proceeding record in format `RRRR-MM-DDTHH:MM:SS` |
| **LastRecordDate** | date of the latest proceeding record in format `RRRR-MM-DDTHH:MM:SS` |
| **RUState** | status according to the Insolvency register |
| **RUStateDate** | status date according to the Insolvency register in format `RRRR-MM-DDTHH:MM:SS` |
| **OVState** | status according to the Commercial Bulletin |
| **OVStateDate** | status date according to the Commercial Bulletin in format `RRRR-MM-DDTHH:MM:SS` |
| **EnterDate** | proceeding start date in format `RRRR-MM-DDTHH:MM:SS` |
| **ExitDate** | proceeding termination date in format `RRRR-MM-DDTHH:MM:SS` |
| **EndState** | status of the proceeding terminatiom |
| **EndReason** | reason for termination of the proceeding |
| **Deadlines** | list of current Deadlines [`Deadline`](#Deadline) |
| **FinstatURL** |link to the proceeding on www.finstat.sk |