# Elite API
API slúži na vyžiadanie rozšíreného detaily firmy [`ExtendedResult`](#ExtendedResult)

## Požiadavka extended
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://www.finstat.sk/api/extended```<br />
> **Hash parameter**: {ico}

### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/extended?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
#### ExtendedResult

[](../../../common/responses/basic-sk.md ':include')

[](../../../common/responses/premium-common-sk.md ':include')

[](../../../common/responses/elite-sk.md ':include')

[](../../../common/responses/icdphadditional-sk.md ':include')

[](../../../common/responses/judgementindicator-sk.md ':include')

[](../../../common/responses/bankaccount-sk.md ':include')

[](../../../common/responses/debt-sk.md ':include')

[](../../../common/responses/receivable-sk.md ':include')

[](../../../common/responses/paymentorder-sk.md ':include')

[](../../../common/responses/office-sk.md ':include')

[](../../../common/responses/subject-sk.md ':include')

[](../../../common/responses/contactsource-sk.md ':include')

[](../../../common/responses/structuredname-sk.md ':include')

[](../../../common/responses/judgementcount-sk.md ':include')

[](../../../common/responses/ratio-sk.md ':include')

[](../../../common/responses/item-sk.md ':include')

[](../../../common/responses/distraintsauthorizationinfo-sk.md ':include')

[](../../../common/responses/creditscotestate-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/elite.md ':include')

[](../../../common/texts/anonymized-sk.md ':include')

[](../../../common/examples/detail-an.md ':include')