# API na sledovanie dôležitých udalostí (Dátumy narodenia)

## Požiadavka MonitoringDateProceedings
Požiadavka na zoznam konaní osôb [`ProceedingResult`](#ProceedingResult) za posledných 10 dní 

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringdateproceedings```<br />
> **Hash parameter**: dateproceedings

### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringdateproceedings?apikey=YourAPIKey&hash=7b0b6f41052ed12cb0438c75d335ac7e578ec8cb6a9ed428301e6d95f4896e94&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
[](../../../common/responses/monitoring-proceedings-sk.md ':include')

[](../../../common/responses/fullddress-sk.md ':include')

[](../../../common/responses/personaddress-sk.md ':include')

[](../../../common/responses/administratoraddress-sk.md ':include')

[](../../../common/responses/court-sk.md ':include')

[](../../../common/responses/issuedperson-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/monitoring-proceeding.md ':include')
