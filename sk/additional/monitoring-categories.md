## Požiadavka MonitoringCategories
Požiadavka zistenie zoznamu kategórií užívateľa
> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringcategories```<br />
> **Hash parameter**: monitoringcategories

### Parametre
[](../parts/parameters.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/monitoringcategories?apikey=YourAPIKey&hash=05e261e4d5a50ceecfc584ca85623595ceae8b1de2a40252ea1472f13361b564&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
Zoznam hodnôt `MonitoringCategory`

| Parameter | Popis |
| ----------- | ----------- |
| **Category** | unikátny identifikátor skupiny |
| **Name** | uživateľský názov skupiny |
