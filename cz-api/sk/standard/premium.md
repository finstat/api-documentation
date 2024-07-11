# Premium API
API slúži na vyžiadanie základného detailu firmy [`DetailResult`](#DetailResult)

## Požiadavka detail
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://cz.finstat.sk/api/detail```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/detail```<br />
> **Hash parameter**: {ico}
### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.cz/api/detail?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
#### DetailResult
[](../../../common/responses/basiccz-sk.md ':include')

[](../../../common/responses/premiumcz-common-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/premium-cz.md ':include')