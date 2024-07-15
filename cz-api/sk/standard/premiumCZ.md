# PremiumCZ API
API slúži na vyžiadanie detailu firmy [`PremiumCZResult`](#PremiumCZResult)

---
## Požiadavka premiumcz
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://cz.finstat.sk/api/premiumcz```<br />
> **Hash parameter**: {ico}
<!-- > **Dopytovaná URL**: ```https://www.finstat.cz/api/premiumcz```<br /> -->

### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://cz.finstat.sk/api/premiumcz?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
#### PremiumResult

[](../../../common/responses/basiccz-sk.md ':include')

[](../../../common/responses/premiumcz-common-sk.md ':include')

[](../../../common/responses/premiumcz-sk.md ':include')

[](../../../common/responses/bankaccount-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/premiumcz-cz.md ':include')