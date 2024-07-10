##### Spoločné ultimate parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **EmployeesNumber** | presný počet zamestnancov pre aktuálny rok finančných dát (ActualYear) môže byť prázdny, ak nebol uvedený |
| **ORSection** | OR - oddiel |
| **ORInsertNo** | OR – vložka č. |
| **Persons** |  zoznam osôb vyparsovaných z ORSR [`Person`](#Person)|
| **RpvsPerson** | zoznam osôb vyparsovaných z RPVS [`RpvsPerson`](#RpvsPerson)|
| **PaybackRange** | rozsah splatenia |
| **RegistrationCourt** | súd kde bola spoločnosť registrovaná  [`CourtAddress`](#CourtAddress)|
| **WebPages** | zoznam webových stránok firmy `string` |
| **AddressHistory** | zoznam historických adries firmy [`HistoryAddress`](#HistoryAddress) |
| **StatutoryAction** | konanie štatutárov text |
| **ProcurationAction** | konanie prokúry text |
| **Bankrupt** | informácia o konkurze [`BankruptResult`](#ProceedingResult) |
| **Restructuring** | informácia o reštrukturalizácii [`RestructuringResult`](#ProceedingResult) |
| **Liquidation** | informácia o likvidácii [`LiquidationResult`](#LiquidationResult) |
| **ORCancelled** | dátum zrušenia firmy podľa Obchodného registra |
| **OtherProceeding** | informácia o inom konaní (o oddlžení) [`ProceedingResult`](#ProceedingResult) |
| **RPOPersons** | zoznam osôb vyparsovaných z RPO  [`RpoPerson`](#RpoPerson) |
| **DistraintsAuthorizations** | Zoznam aktívnych poverení na výkon exekúcie pre povinného [`DistraintsAuthorizationDetail`](#DistraintsAuthorizationDetail) |