# UltimateCZ API
API slúži na vyžiadanie detailu firmy [`UltimateCZResult`](#UltimateCZResult). Obsahuje všetky parametre PremiumCZ a EliteCZ a parametre UltimateCZ.

---
## Požiadavka ultimatecz
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://cz.finstat.sk/api/ultimatecz```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/ultimatecz```<br />
> **Hash parameter**: {ico}

### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameterscz-sk.md ':include')

[](../../../common/parameters/languagecz-sk.md ':include')


> **Príklad volania:** ```https://cz.finstat.sk/api/ultimatecz?ico=00177041&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
#### UltimateCZResult

[](../../../common/responses/basiccz-sk.md ':include')

[](../../../common/responses/premiumcz-common-sk.md ':include')

[](../../../common/responses/premiumcz-sk.md ':include')

[](../../../common/responses/elitecz-sk.md ':include')

[](../../../common/responses/ultimatecz-sk.md ':include')

[](../../../common/responses/bankaccount-sk.md ':include')

[](../../../common/responses/turnovercategory-sk.md ':include')

[](../../../common/responses/financialindicatorcz-sk.md ':include')

[](../../../common/responses/cznace-sk.md ':include')

[](../../../common/responses/contactcz-sk.md ':include')

[](../../../common/responses/officescz-sk.md ':include')

[](../../../common/responses/officecz-sk.md ':include')

[](../../../common/responses/vehiclefleet-sk.md ':include')

[](../../../common/responses/vehiclefleetitem-sk.md ':include')

[](../../../common/responses/isirdeed-sk.md ':include')

[](../../../common/responses/receivableapplication-sk.md ':include')

[](../../../common/responses/isirstatus-sk.md ':include')

[](../../../common/responses/creditscorecz-sk.md ':include')

[](../../../common/responses/creditscotestate-sk.md ':include')

[](../../../common/responses/orcrperson-sk.md ':include')

[](../../../common/responses/personfunction-sk.md ':include')

[](../../../common/responses/structuredname-sk.md ':include')

[](../../../common/responses/rzpperson-sk.md ':include')

[](../../../common/responses/subject-sk.md ':include')

[](../../../common/responses/filedinsolvencyclaims-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

> **Poznámka:** kódy (`TaxPayer`, `Status`, `Type`, `Function`, `State`, …) sú v XML aj JSON vždy texty. Popisy (`…Text`, `LegalForm`, `CzNaceText`, …) sú na cz.finstat.sk po slovensky, na www.finstat.cz podľa parametra `lang`.

# Príklad XML odpovede
Mená, dátumy narodenia a adresy fyzických osôb sú v príklade nahradené vymyslenými údajmi.

[](../../../common/examples/ultimatecz-cz.md ':include')
