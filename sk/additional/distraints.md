# API na vyhľadávanie exekúcií
Informácie o exekúciách priamo vo Vašom informačnom systéme

---
## Požiadavka RequestDistraintSearch
Spoplatnená požiadavka.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/requestdistraintsearch```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **search**<br />*[povinný]* | formát `{ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}`. <br />Kde:<table><tr><td>**ico**</td><td>IČO</td></tr><tr><td>**surname**</td><td>Priezvisko</td></tr><tr><td>**dateOfBirth**</td><td>Dátum narodenia</td></tr><tr><td>**city**</td><td>Obec</td></tr><tr><td>**companyName**</td><td>Názov spoločnosti</td></tr><tr><td>**fileReference**</td><td>Spisová značka súdu</td></tr></table> Nechcené stačí nastaviť ako prázdne resp. `null`.|


[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/requestdistraintsearch```

### Popis odpovede
[](../parts/distraint-result.md ':include')

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/distraint-result.md ':include')

## Požiadavka RequestDistraintDetail
Spoplatnená požiadavka

> **Dopytovaná URL**: ```https://www.finstat.sk/api/requestdistraintdetail```<br />
> **Hash parameter**: {token}{zodnam ids spojených do stringu bez oddeľovacov}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |
| **ids**<br />*[povinný]* | zoznam DetailId iddelené čiarkami |


[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/requestdistraintdetail```

### Popis odpovede
[](../parts/distraint-detail.md ':include')

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede

[](../../examples/distraint-detail.md ':include')

## Požiadavka RequestDistraintResults
Požiadavka vracia posledný historický dopyt podľa kritéria

> **Dopytovaná URL**: ```https://www.finstat.sk/api/requestdistraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **search**<br />*[povinný]* | formát `{ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}`. <br />Kde:<table><tr><td>**ico**</td><td>IČO</td></tr><tr><td>**surname**</td><td>Priezvisko</td></tr><tr><td>**dateOfBirth**</td><td>Dátum narodenia</td></tr><tr><td>**city**</td><td>Obec</td></tr><tr><td>**companyName**</td><td>Názov spoločnosti</td></tr><tr><td>**fileReference**</td><td>Spisová značka súdu</td></tr></table> Nechcené stačí nastaviť ako prázdne resp. `null`.|


[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/requestdistraintresults```

### Popis odpovede
[](../parts/distraint-result.md ':include')

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/distraint-result.md ':include')

## Požiadavka RequestDistraintResultsByToken
Požiadavka vracia posledný historický dopyt podľa token-u.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/requestdistraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |


[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/requestdistraintresultsbytoken```

### Popis odpovede
[](../parts/distraint-result.md ':include')

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/distraint-result.md ':include')

## Požiadavka RequestDistraintStoredDetail
Požiadavka vracia uložený detail exekúcie.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/requestdistraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **id**<br />*[povinný]* | StoredDetailId |


[](../parts/parameters.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/requestdistraintstoreddetail```

### Popis odpovede
[](../parts/distraint-detail.md ':include')

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/distraint-detail.md ':include')