# Premium API
API slúži na vyžiadanie základného detailu firmy

---
## Požiadavka detail
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://www.finstat.sk/api/detail```<br />
> **Hash parameter**: {ico}
### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/detail?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```
### Popis odpovede

Dopyt vráti odpoveď s nasledulúcimi parametrami:

[](../../../common/responses/basic-sk.md ':include')

[](../../../common/responses/premium-common-sk.md ':include')

[](../../../common/responses/premium-sk.md ':include')

[](../../../common/responses/icdphadditional-sk.md ':include')

[](../../../common/responses/judgementindicator-sk.md ':include')

[](../../../common/responses/bankaccount-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
[](../../../common/examples/premium.md ':include')

[](../../../common/texts/anonymized-sk.md ':include')

[](../../../common/examples/detail-an.md ':include')