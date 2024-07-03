# API na synchronizáciu portfólia (Dátumy narodenia)

---
[](monitoring-categories.md ':include')

#### Návratové HTTP error kódy:

[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-categories.md ':include')

## Požiadavka AddDateToMonitoring
Požiadavka na pridanie dátumu narodenia osoby do monitoringu

> **Dopytovaná URL**: ```https://www.finstat.sk/api/adddatetomonitoring```<br />
> **Hash parameter**: {date}

### Parametre
[](../../../common/parameters/monitoring-addremove-date-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/adddatetomonitoring?date=9.2.2024&apikey=YourAPIKey&hash=b8c62bab2473673ae1c9a461cab2dd824d86da1d62745290dbb110140075b076&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Požiadavka vráti odpoveď `true` pri úspešnom a `false`  pri neúspešnom pridaní do monitoringu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RemoveDateFromMonitoring
Požiadavka na odobratie dátumu narodenia osoby z monitoringu

> **Dopytovaná URL**: ```https://www.finstat.sk/api/removedatefrommonitoring```<br />
> **Hash parameter**: {date}

### Parametre
[](../../../common/parameters/monitoring-addremove-date-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/removedatefrommonitoring?date=9.2.2024&apikey=YourAPIKey&hash=b8c62bab2473673ae1c9a461cab2dd824d86da1d62745290dbb110140075b076&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Požiadavka vráti odpoveď `true` pri úspešnom a `false`  pri neúspešnom pridaní do monitoringu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')


## Požiadavka MonitoringDateList
Požiadavka na aktuálny zoznam dátumov narodenia osôb v monitoringu

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringdatelist```<br />
> **Hash parameter**: datelist

### Parametre
[](../../../common/parameters/monitoring-category-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringdatelist?apikey=YourAPIKey&hash=3cb3d0526473367453ee5779e985a33194356df01551e45ebc2d2f873df79c0e&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Odpoveď obsahuje zoznam aktuálnych dátumov narodenia osôb v monitoringu.

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-datelist.md ':include')

## Požiadavka MonitoringDateReport
Požiadavka na zoznam udalostí osôb za posledných 30 dní pre aktuálne monitorované osoby

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringdatereport```<br />
> **Hash parameter**: datereport

### Parametre
[](../../../common/parameters/monitoring-category-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringdatereport?apikey=YourAPIKey&hash=a0c1760f69233637d6238dcac01fbb4226d69f461a4ca72bd1c8576dfd3f27d4&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../../../common/responses/monitoring-date-sk.md ':include')

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-datereport.md ':include')