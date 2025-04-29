##### Spoločné ultimatediff parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **Country**| krajina sídla firmy (ak prázdne, tak Slovensko) |
| **RpvsInsert** | indikácia, či je firma aktuálne zapísaná v RPVS/ číslo vložky – môže byť prázdny |
| **RpvsUrl** | odkaz na záložku Osoby vo firme na portáli FinStat.sk – môže byť prázdny |
| **JudgementIndicators** | zoznam indikátorov súdnych rozhodnutí [`JudgementIndicator`](#JudgementIndicator) – môže byť prázdny |
| **JudgementFinstatLink** | odkaz na súdne rozhodnutia, ak existujú – môže byť prázdny |
| **KarUrl** | Url na zoznam konkurzov a reštrukturalizácií firmy – môže byť prázdny |
| **HasDebt** | Príznak, či firma má aktuálny dlh, pohľadávku štátu alebo komerčnú pohľadávku (`true/false`) |
| **DebtUrl** | Url na zoznam dlhov a pohľadávok firmy – môže byť prázdny |
| **BasicCapital** | základné imanie |
| **StateReceivables** | zoznam pohľadávok [`ReceivableDebt`](#ReceivableDebt) |
| **HasDisposal** | príznak, či firma je v likvidácii `true/false` |
| **DisposalUrl** | url na likvididácie firmy |
| **SelfEmployed** | príznak, či je subjekt živnostník `true/false` |
| **Offices** | zoznam pobočiek [`Office`](#Office) – môže byť prázdny |
| **Subjects** | zoznam predmetov podnikania [`Subject`](#Subject) – môže byť prázdny |
| **ContactSources** | zoznam zdrojov jednotlivých kontaktov (položky Emails, Phones) [`ContactSource`](#ContactSource) – môže byť prázdny |
| **StructuredName** | len pri živnostníkoch, inak nie je hodnota dostupná - obsahuje rozdelený obchodný názov na jednotlivé časti [`StructuredName`](#StructuredName) |
| **JudgementCounts** | zoznam počtov súdnych rozhodnutí [`JudgementCount`](#JudgementCount) – môže byť prázdny |
| **JudgementLastPublishedDate** | Dátum posledného súdneho rozhodnutia |
| **SalesCategory** | kategória obratu |
| **EmployeesNumber** | presný počet zamestnancov pre aktuálny rok finančných dát (ActualYear) môže byť prázdny, ak nebol uvedený |
| **ORSection** | OR - oddiel |
| **ORInsertNo** | OR – vložka č. |
| **Persons** |  zoznam osôb vyparsovaných z ORSR [`Person`](#Person)|
| **RpvsPersons** | zoznam osôb vyparsovaných z RPVS [`RpvsPerson`](#RpvsPerson)|
| **PaybackRange** | rozsah splatenia |
| **RegistrationCourt** | súd kde bola spoločnosť registrovaná  [`Court`](#Court)|
| **WebPages** | zoznam webových stránok firmy `string` |
| **AddressHistory** | zoznam historických adries firmy [`HistoryAddress`](#HistoryAddress) |
| **StatutoryAction** | konanie štatutárov text |
| **ProcurationAction** | konanie prokúry text |
| **Bankrupt** | informácia o konkurze [`BankruptResult`](#BankruptResult) |
| **Restructuring** | informácia o reštrukturalizácii [`RestructuringResult`](#RestructuringResult) |
| **Liquidation** | informácia o likvidácii [`LiquidationResult`](#LiquidationResult) |
| **ORCancelled** | dátum zrušenia firmy podľa Obchodného registra vo formáte `RRRR-MM-DDTHH:MM:SS`|
| **OtherProceeding** | informácia o inom konaní (o oddlžení) [`ProceedingResult`](#ProceedingResult) |
| **ORRemoved** | dátum odobratia firmy podľa Obchodného registra vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **EmployeeYear** | rok posledného záznamu o presnom počte zamestnancov |
| **ORLiquidationDate** | dátum likvidácie podľa Obchodného registra vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **IncorporationDates** | zoznam dátumov vzniky firmy podľa zdroja [`IncorporationDate`](#IncorporationDate) |
| **DissolutionDates** | zoznam dátumov zániku firmy podľa zdroja [`DissolutionDate`](#DissolutionDate) ||