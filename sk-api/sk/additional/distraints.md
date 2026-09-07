# API na vyhľadávanie exekúcií
Informácie o exekúciách priamo vo Vašom informačnom systéme

## Požiadavka RequestDistraintSearch
Vráti zoznam náhľadov exekúcii na základe vyhľadávaných kritérií [`DistraintResult`](#DistraintResult).
Spoplatnená požiadavka.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintsearch```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre

[](../../../common/parameters/distraint-search-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintsearch```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RequestDistraintDetail
Vráti zoznam náhľadov exekúcii na základe vyhľadávaných id [`DistraintDetail`](#DistraintDetail). Spoplatnená požiadavka

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintdetail```<br />
> **Hash parameter**: {token}{zoznam ids spojených do stringu bez oddeľovacov}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |
| **ids**<br />*[povinný]* | zoznam DetailId oddelené čiarkami |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintdetail```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RequestDistraintResults
Požiadavka vracia posledný historický dopyt [`DistraintResult`](#DistraintResult) podľa kritéria

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre

[](../../../common/parameters/distraint-search-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintresults```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RequestDistraintResultsByToken
Požiadavka vracia posledný historický dopyt [`DistraintResult`](#DistraintResult) podľa token-u.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintresultsbytoken```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RequestDistraintStoredDetail
Požiadavka vracia uložený detail exekúcie [`DistraintDetail`](#DistraintDetail).

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **id**<br />*[povinný]* | StoredDetailId |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintstoreddetail```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovedí
[](../../../common/responses/distraint-result-sk.md ':include')

[](../../../common/responses/distraintpreview-sk.md ':include')

[](../../../common/responses/distraint-detail-sk.md ':include')

[](../../../common/responses/debtor-sk.md ':include')

[](../../../common/responses/bailiff-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklady XML odpovede
[](../../../common/examples/distraint-result.md ':include')

[](../../../common/examples/distraint-detail.md ':include')