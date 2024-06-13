# API na sledovanie dôležitých udalostí (IČO)

---
## Požiadavka MonitoringProceedings
Požiadavka na zoznam konaní firiem za posledných 10 dní 

> **Dopytovaná URL**: ```https://www.finstat.sk/api/monitoringproceedings```<br />
> **Hash parameter**: proceedings
### Parametre

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/monitoringproceedings?apikey=YourAPIKey&hash=7e78a38b3f54bb2d10fae11aa2f15cdddc97744da85046423797d5fdbc1abf65&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede
[](../../../common/responses/monitoring-sk-proceedings.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/monitoring-proceeding.md ':include')