##### Doplnené parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **VATNumber** | daňová identifikácia |
| **TaxPayer** | ozačenie typu platcovstva DPH – môže byť prázdny <ul><li>Platce</li><li>IdentifikovanaOsoba</li><li>OsobaIdentifikovanaKDani</li></ul> |
| **LegalFormCode** | právna forma kód - môže byť prázdny |
| **OwnershipTypeCode** | druh vlastníctva kód - môže byť prázdny |
| **BankAccounts** | zoznam aktuálne nahlásených účtov [`BankAccount`](#BankAccount) – môže byť prázdny |
| **Unreliability** | ozačenie či je nedôverihodný platca /osoba|
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>Obchodný register XXXX súdu XXXXX, oddiel: xxx, vložka č.xxxx/x</li></ul>|
| **TradeLicensingOffice** | evidujúci úrad z Registra živnostenského podnikania - môže byť prázdny <ul><li>XXXXX</li></ul>|
| **ActualYear**| rok poslednej finančnej závierky |
| **SalesActual**| hodnota tržieb za posledný dosupný rok |
| **ProfitActual**| hodnota zisku za posledný dosupný rok|
| **Sales**| príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze. Vymenovaný typ (`Unknown, Up, Down`) |
| **Profit**| príznak nárastu/poklesu zisku firmy medzi posledným a predposledným rokom v databáze. Vymenovaný typ (`Unknown, Up, Down, Loss`) stav loss znamená, že firma vykázala za posledný rok stratu |