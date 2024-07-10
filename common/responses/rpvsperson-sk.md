#### RpvsPerson
| Parameter | Popis |
| ----------- | ----------- |
| **FullName** | celé meno - v prípade že je to firma, tak obsahuje názov firmy |
| **Street** | ulica osoby |
| **StreetNumber** | popisné čislo budovy |
| **City** | mesto |
| **District** | okres |
| **Region** | kraj |
| **Country** | štát |
| **Ico** | IČO osoby v prípade firmy - môže byť prázdne |
| **BirthDate** | dátum narodenia |
| **DetectedFrom** | dátum, od ktorého je vo finstat.sk táto osoba na danej pozícii detekovaná (obsahuje dátum poslednej zmeny) vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | dátum, do ktorého je detekovaná v prípade historických dát vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Functions** | zoznam funkcií osoby vo firme [`FunctionAssigment`](#FunctionAssigment) |
| **StructuredName** | obsahuje rozdelený obchodný názov na jednotlivé časti [`StructuredName`](#StructuredName) |