# API na vyhľadávanie exekúcií
Informácie o exekúciách priamo vo Vašom informačnom systéme

## Požiadavka DistraintSearch
Vráti zoznam náhľadov exekúcii na základe vyhľadávaných kritérií [`DistraintResult`](#DistraintResult).
Spoplatnená požiadavka.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintsearch```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre

[](../../../common/parameters/distraint-search-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintsearch```

> **Cena:** účtuje sa ako **1 dopyt** (jedna cenová jednotka podľa Vašej licencie).

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

[](../../../common/http/errorcodes-sk-distraint.md ':include')

## Požiadavka DistraintDetail
Vráti detaily exekúcií na základe vyhľadávaných id.
Odpoveďou je obal [`DistraintDetailResults`](#DistraintDetailResults) so zoznamom
**DistraintDetails**, ktorého položky sú typu [`DistraintDetailResult`](#DistraintDetailResult) —
a to aj v prípade, že sa dopytuje jediné id.
Spoplatnená požiadavka.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintdetail```<br />
> **Hash parameter**: {token}{zoznam ids spojených do stringu bez oddeľovacov}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |
| **ids**<br />*[povinný]* | zoznam DetailId oddelené čiarkami |

##### Validácie parametrov
Nesplnenie ktorejkoľvek z nich vráti **HTTP 400** a dôvod v texte odpovede:

| Validácia | Text odpovede |
| ----------- | ----------- |
| `token` musí byť vyplnený | ```'token' parameter not specified!``` |
| `ids` musí obsahovať aspoň jedno **číselné** id; nečíselná hodnota v zozname zneplatní celý parameter | ```'ids' parameter not valid!``` |
| po odstránení duplicít môže zoznam `ids` obsahovať **maximálne 200** identifikátorov | ```'ids' parameter maximum size of 200 identifiers exceeded!``` |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintdetail```

> **Cena:** požiadavka sa **neúčtuje ako jeden dopyt** — účtuje sa **počet unikátnych
identifikátorov** v parametri `ids`. Dopyt s 10 rôznymi id sa teda účtuje ako 10 dopytov.
Duplicitné id sa pred účtovaním odstránia. Ak na požadovanú sumu nie je dostatok kreditu,
vráti sa **402** a dopyt do registra sa vôbec nevykoná.

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

[](../../../common/http/errorcodes-sk-distraint.md ':include')

## Požiadavka DistraintResults
Požiadavka vracia posledný historický dopyt [`DistraintResult`](#DistraintResult) podľa kritéria

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintresults```<br />
> **Hash parameter**: {ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}

### Parametre

[](../../../common/parameters/distraint-search-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintresults```

> **Cena:** požiadavka sa neúčtuje z kreditu, číta sa už zaplatený historický dopyt.
Naďalej sa však počíta do denného a mesačného limitu API volaní.

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

[](../../../common/http/errorcodes-sk-distraint.md ':include')

## Požiadavka DistraintResultsByToken
Požiadavka vracia posledný historický dopyt [`DistraintResult`](#DistraintResult) podľa token-u.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintresultsbytoken```<br />
> **Hash parameter**: {token}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **token**<br />*[povinný]* | DetailToken |

Nevyplnený `token` vráti **HTTP 400** s textom ```'token' parameter not specified!```.

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintresultsbytoken```

> **Cena:** požiadavka sa neúčtuje z kreditu, číta sa už zaplatený historický dopyt.
Naďalej sa však počíta do denného a mesačného limitu API volaní.

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

[](../../../common/http/errorcodes-sk-distraint.md ':include')

## Požiadavka DistraintStoredDetail
Požiadavka vracia už uložený detail exekúcie.
Odpoveďou je obal [`DistraintDetailResults`](#DistraintDetailResults) so zoznamom
**DistraintDetails**, ktorého položky sú typu [`DistraintDetailResult`](#DistraintDetailResult).
Keďže sa dopytuje jedno `id`, zoznam obsahuje najviac jednu položku; ak sa detail nenašiel,
vráti sa prázdny element ```<DistraintDetails />```.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/distraintstoreddetail```<br />
> **Hash parameter**: {id}

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **id**<br />*[povinný]* | StoredDetailId |

Nevyplnené `id` vráti **HTTP 400** s textom ```'id' parameter not specified!```.

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/distraintstoreddetail```

> **Cena:** požiadavka sa neúčtuje z kreditu, číta sa už zaplatený detail.
Naďalej sa však počíta do denného a mesačného limitu API volaní.

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

[](../../../common/http/errorcodes-sk-distraint.md ':include')

# Štruktúra odpovedí
[](../../../common/responses/distraint-result-sk.md ':include')

[](../../../common/responses/distraintpreview-sk.md ':include')

[](../../../common/responses/distraint-detail-results-sk.md ':include')

[](../../../common/responses/distraint-detail-sk.md ':include')

[](../../../common/responses/debtor-sk.md ':include')

[](../../../common/responses/bailiff-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklady XML odpovede
[](../../../common/examples/distraint-result.md ':include')

[](../../../common/examples/distraint-detail.md ':include')