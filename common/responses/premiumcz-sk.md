##### Doplnené parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **VatNumber** | daňová identifikácia (DIČ) |
| **TaxPayer** | označenie typu registrácie k DPH – môže byť prázdny: `VatPayer` (platca DPH), `IdentifiedPerson` (identifikovaná osoba), `PersonIdentifiedForTax` (osoba identifikovaná k dani). Na `cz.finstat.sk` vracajú Free, Detail a PremiumCZ dočasne, do vydania nového CZ API, pôvodné hodnoty: `Platce`, `IdentifikovanaOsoba`, `OsobaIdentifikovanaKDani` |
| **LegalFormCode** | právna forma kód - môže byť prázdny |
| **OwnershipCode** | druh vlastníctva kód - môže byť prázdny |
| **EmployeeCode** | kód kategórie počtu zamestnancov (text kategórie je v `EmployeeCount`) – môže byť prázdny |
| **BankAccounts** | zoznam aktuálne nahlásených účtov [`BankAccount`](#BankAccount) – môže byť prázdny |
| **UnReliability** | označenie, či je subjekt nespoľahlivý platca alebo nespoľahlivá osoba (`true`) – môže byť prázdny |
| **RegisterNumberText** | textový popis registračných údajov, iba pri subjektoch, ktoré nie sú živnostníkmi – môže byť prázdny <ul><li>Obchodný register XXXX súdu XXXXX, oddiel: xxx, vložka č.xxxx/x</li></ul>|
| **TradeLicensingOffice** | mesto evidujúceho úradu z Registra živnostenského podnikania, iba pri živnostníkoch – môže byť prázdny <ul><li>XXXXX</li></ul>|
| **ActualYear**| rok poslednej finančnej závierky – môže byť prázdny. Vracia ho iba PremiumCZ; EliteCZ a UltimateCZ ho nevracajú (hodnoty za jednotlivé roky sú vo `FinancialIndicators`) |
| **SalesActual**| hodnota tržieb za posledný dostupný rok – môže byť prázdny. Vracia ho iba PremiumCZ; EliteCZ a UltimateCZ ho nevracajú (hodnoty za jednotlivé roky sú vo `FinancialIndicators`) |
| **ProfitActual**| hodnota zisku za posledný dostupný rok – môže byť prázdny. Vracia ho iba PremiumCZ; EliteCZ a UltimateCZ ho nevracajú (hodnoty za jednotlivé roky sú vo `FinancialIndicators`) |
| **Sales**| príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze; ak predposledný rok chýba, `Up`. Vymenovaný typ (`Unknown, Up, Down`). PremiumCZ ho v JSON vracia ako číslo (`0` Unknown, `1` Up, `2` Down), EliteCZ a UltimateCZ ako text a bez finančných údajov (`Unknown`) ho nevracajú |
| **Profit**| príznak nárastu/poklesu zisku firmy medzi posledným a predposledným rokom v databáze; ak predposledný rok chýba, `Up`. Vymenovaný typ (`Unknown, Up, Down, Loss`), stav `Loss` znamená, že firma vykázala za posledný rok stratu. PremiumCZ ho v JSON vracia ako číslo (`0` Unknown, `1` Up, `2` Down, `3` Loss), EliteCZ a UltimateCZ ako text a bez finančných údajov (`Unknown`) ho nevracajú |
| **TurnoverCategory** | kategória obratu za posledný dostupný rok [`TurnoverCategory`](#TurnoverCategory) – môže byť prázdny |
| **SuspendedAsPersonUntil** | pri živnostníkoch, ktorí majú pozastavené všetky predmety podnikania: najskorší dátum, do ktorého je pozastavenie, vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
