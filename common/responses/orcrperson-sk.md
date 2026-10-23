#### ORCRPerson
Štruktúra je rovnaká ako `Person` v SK Ultimate API, funkcie sú v tvare [`Function`](#Function) a pribudol parameter `Ico`.

| Parameter | Popis |
| ----------- | ----------- |
| **Street** | ulica |
| **StreetNumber** | popisné číslo budovy |
| **ZipCode** | PSČ |
| **City** | mesto |
| **Country** | štát |
| **Region** | kraj |
| **District** | okres |
| **FullName** | celé meno vrátane titulov, pri firme jej názov |
| **DetectedFrom** | dátum, od ktorého je osoba na danej pozícii detekovaná, vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | dátum, do ktorého je osoba detekovaná, vo formáte `RRRR-MM-DDTHH:MM:SS` – pri aktívnych osobách prázdny |
| **StructuredName** | meno rozdelené na časti [`StructuredName`](#StructuredName) |
| **Functions** | zoznam funkcií osoby vo firme [`Function`](#Function) |
| **BirthDate** | dátum narodenia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **DepositAmount** | výška vkladu – môže byť prázdny |
| **PaybackRange** | rozsah splatenia vkladu – môže byť prázdny |
| **PartnersSharePercentage** | podiel spoločníka v percentách – môže byť prázdny |
| **Ico** | IČO osoby, ak ide o firmu – môže byť prázdne |
