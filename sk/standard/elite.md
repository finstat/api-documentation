# Elite API
API slúži na vyžiadanie rozšíreného detaily firmy

---
## Požiadavka extended
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://www.finstat.sk/api/extended```<br />
> **Hash parameter**: {ico}
### Parametre
[](../parts/parameters-detail.md ':include')

[](../parts/parameters.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/extended?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```
### Popis odpovede

Dopyt vráti odpoveď s nasledulúcimi parametrami:

[](../parts/api-basic.md ':include')

[](../parts/api-premium.md ':include')

[](../parts/api-elite.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../parts/httperrorcodes-detail.md ':include')

[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
[](../../examples/elite.md ':include')

[](../parts/anonymized.md ':include')

[](../../examples/detail-an.md ':include')