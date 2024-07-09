##### Doplnené parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **VATNumber** | daňová identifikácia |
| **TaxPayer** | ozačenie typu platcovstva DPH – môže byť prázdny <ul><li>Platce</li><li>IdentifikovanaOsoba</li><li>OsobaIdentifikovanaKDani</li></ul> |
| **LegalFormCode** | právna forma kód - môže byť prázdny |
| **OwnershipTypeCode** | druh vlastníctva kód - môže byť prázdny |
| **BankAccounts** | Zoznam aktuálne nahlásených účtov [`BankAccount`](#BankAccount) – môže byť prázdny |
| **Uneliability** | ozačenie či je nedôverihodný platca /osoba|
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>pre s.r.o. v tvare: Zapísaná na Okr. súde XXXXX, odd. Sro, vl.č.xxxx/L</li><li>pre živnostníka: Číslo živn.registra: xxx-xxxx, okresný úrad XXXXX </li></ul>|
| **ActualYear**| rok poslednej finančnej závierky |
| **SalesActual**| hodnota tržieb za posledný dosupný rok |
| **ProfitActual**| hodnota zisku za posledný dosupný rok|
| **Sales**| príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down) |
| **Profit**| príznak nárastu/poklesu zisku firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down, Loss) stav loss znamená, že firma vykázala za posledný rok stratu |