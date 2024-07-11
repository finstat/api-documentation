# API na synchronizáciu portfólia (IČO)

[](monitoring-categories.md ':include')

#### Návratové HTTP error kódy:

[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka AddToMonitoring
Požiadavka na pridanie firmy do monitoringu.
Dopyt vráti odpoveď `true` pri úspešnom a `false`  pri neúspešnom pridaní do monitoringu

> **Dopytovaná URL**: ```https://cz.finstat.sk/api/addtomonitoring```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/addtomonitoring```<br />
> **Hash parameter**: {ico}

### Parametre
[](../../../common/parameters/monitoring-addremove-ico-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://cz.finstat.sk/api/addtomonitoring?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka RemoveFromMonitoring
Požiadavka na odobratie firmy z monitoringu.
Dopyt vráti odpoveď `true` pri úspešnom a `false`  pri neúspešnom pridaní do monitoringu

> **Dopytovaná URL**: ```https://cz.finstat.sk/api/removefrommonitoring```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/removefrommonitoring```<br />
> **Hash parameter**: {ico}

### Parametre
[](../../../common/parameters/monitoring-addremove-ico-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/removefrommonitoring?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Požiadavka MonitoringList
Požiadavka na aktuálny zoznam firiem v monitoringu

> **Dopytovaná URL**: ```https://cz.finstat.sk/api/monitoringlist```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/monitoringlist```<br />
> **Hash parameter**: list

### Parametre
[](../../../common/parameters/monitoring-category-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringlist?apikey=YourAPIKey&hash=da32661cb223d07c2e1bbc8390ab559503e7d937a21e9107445f82f02b73ad42&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-list.md ':include')

## Požiadavka MonitoringReport
Požiadavka na zoznam udalostí firiem [`Monitoring`](#Monitoring) za posledných 30 dní pre aktuálne monitorované firmy

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringreport```<br />
> **Hash parameter**: report

### Parametre
[](../../../common/parameters/monitoring-category-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringreport?apikey=YourAPIKey&hash=816fa3eb97d4acec7ab73f7264a79f5cbe7280f3b0f81dd7b93b8e2981933e0c&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovedí

[](../../../common/responses/monitoring-categories-sk.md ':include')

[](../../../common/responses/monitoring-ico-sk.md ':include')

# Príklade XML odpovedí

[](../../../common/examples/monitoring-categories.md ':include')

[](../../../common/examples/monitoring-list.md ':include')

[](../../../common/examples/monitoring-report.md ':include')
