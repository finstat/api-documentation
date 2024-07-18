# FakturačnéCZ API
API slúži na vyžiadanie jednoduchého detaily firmy [`BasicResult`](#BasicResult)

## Požiadavka basic
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://cz.finstat.sk/api/basic```<br />
> **Hash parameter**: {ico}
<!-- > **Dopytovaná URL**: ```https://www.finstat.cz/api/basic```<br /> -->

### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://cz.finstat.sk/api/basic?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
#### BasicResult
[](../../../common/responses/basiccz-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/invoice-cz.md ':include')

