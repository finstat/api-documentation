# API na sledovanie dôležitých udalostí (Dátumy narodenia)

---
## Požiadavka MonitoringDateProceedings
Požiadavka na zoznam konaní firiem za posledných 10 dní 

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringdateproceedings```<br />
> **Hash parameter**: dateproceedings
### Parametre

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringdateproceedings?apikey=YourAPIKey&hash=7b0b6f41052ed12cb0438c75d335ac7e578ec8cb6a9ed428301e6d95f4896e94&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../../../common/responses/monitoring-sk-proceedings.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-proceeding.md ':include')
