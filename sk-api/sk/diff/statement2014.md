# Denný zmenový súbor na finančné výkazy
Toto API poskytuje možnosť, ako získať prístup k dátam bez nutnosti každý deň dotazovať API na zmeny. API vygeneruje pre každý deň, kedy nastala zmena, zmenový súbor obsahujúci posledné zmeny v závierkach.

API obsahuje informácie o všetkých závierkach. Firmy, u ktorých sa dlho neudiala žiadna zmena, majú závierky v súboroch vygenerovaných po zverejnení poslednej závierky. 

API je inkrementálny export, a tak sa niektoré závierky môžu nachádzať vo viacerých súboroch, kde aktuálna hodnota je vždy v exporte s najnovším dátumom.

## Požiadavka GetListOfStatement2014Diffs
Požiadavka na získanie zoznamu [`DailyDiffList`](#DailyDiffList) všetkých súborov zmien

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getlistofstatement2014diffs```<br />
> **Hash parameter**: prázdny text

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getlistofstatement2014diffs?apikey=YourAPIKey&hash=990ee369d83384c17564fbf5b9ba07684993f3e428df7b7079c9df42a0ef0b1e&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka GetStatement2014File
Požiadavka na stiahnutie konkrétneho súboru zmeny pre konkrétny dátum.
Dopyt vráti dáta požadovaného **.zip** súboru

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatement2014file```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| názov súboru ako je uvedený vo výsledku požiadavky [GetListOfStatement2014Diffs](#požiadavka-getlistofstatement2014diffs) |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatement2014file?filename=statement2014diff-2024-02-08.zip&apikey=YourAPIKey&hash=994141238a0e7a68eabc8028f1f95d4483105b5f259fb7ea82414d8a595a05b1&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-file.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka GetStatement2014Legend

Požiadavka na stiahnutie legendy [`StatementLegendResult`](#StatementLegendResult) kľúčov súboru závierok

> **Dopytovaná URL**: ```https://www.finstat.sk/api/getstatement2014legend```<br />
> **Hash parameter**: {lang}

[](../../../common/parameters/lang-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getstatement2014legend?lang=sk&apikey=YourAPIKey&hash=a8b01632a568dea3e5831c7c1ba0f0dbbe75726828eae91b700806c375996f81&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')


# Štruktúra odpovedí
[](../../../common/responses/diff-sk.md ':include')

[](../../../common/responses/dailydiff-sk.md ':include')

[](../../../common/responses/statementlegendresult-sk.md ':include')

[](../../../common/responses/statementlegendvalue-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklady XML odpovedí
[](../../../common/examples/diff-statement.md ':include')

[](../../../common/examples/diff-statement2014-legend.md ':include')