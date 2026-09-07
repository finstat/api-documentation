| Parameter | Popis |
| ----------- | ----------- |
| **search**<br />*[povinný]* | formát `{ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}`. Nechcené stačí nastaviť ako prázdne alebo `null`.|

- **ico** -	IČO
- **surname** -	priezvisko
- **dateOfBirth** -	dátum narodenia vo formáte `dd.MM.yyyy`
- **city** - obec
- **companyName** -	názov spoločnosti
- **fileReference** - spisová značka súdu

##### Validácie parametra `search`
Nesplnenie ktorejkoľvek z nich vráti **HTTP 400** a dôvod v texte odpovede:

| Validácia | Text odpovede |
| ----------- | ----------- |
| parameter musí obsahovať **presne 6 častí** oddelených znakom `\|` (teda 5 oddeľovačov) aj v prípade, že sú niektoré časti prázdne | ```not all search parameters are specified!``` |
| musí byť vyplnená **aspoň jedna** z hodnôt `ico`, `companyName`, `fileReference`, `surname` | ```search parameters not specified!``` |
| ak je vyplnené `ico`, musí ísť o platné IČO | ```Invalid 'ico' parameter!``` |
| ak je vyplnené `surname`, musí byť vyplnené aj `dateOfBirth` **alebo** `city` | ```parameter 'surname' requires parameter 'dateOfBirth' or 'city'!``` |
| ak je vyplnené `dateOfBirth`, musí byť vo formáte `dd.MM.yyyy` | ```Invalid 'dateOfBirth' parameter, expected format 'dd.MM.yyyy'!``` |

> **Poznámka:** hodnoty jednotlivých častí sa pred vyhodnotením zbavia okrajových medzier.
