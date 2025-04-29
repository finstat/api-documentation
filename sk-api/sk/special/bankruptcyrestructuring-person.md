# API na sledovanie konkurzov (Osoby)

## Požiadavka PersonBankruptcyProceedings
Požiadavka na zoznam konaní osôb [`BankruptcyRestructuring`](#BankruptcyRestructuring).
> **Dopytovaná URL**: ```https://www.finstat.sk/api/PersonBankruptcyProceedings```<br />
> **Hash parameter**: {name}|{surname}|{dateofbirth}

> **Upozornenie**: kôli jednoznačnosti, pre výpočet hashu treba použiť formát pre *{dateofbirth}* `yyyy-mm-dd`

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **name**<br />*[povinný]*| meno osoby |
| **surname**<br />*[povinný]*| priezvisko osoby |
| **dateofbirth**<br />*[povinný]*| dátum narodenia osoby. Podporované formáty `"dd.mm.yyyy", "d.m.yyyy", "dd.m.yyyy", "d.mm.yyyy", "yyyy-mm-dd", "mm/dd/yyyy"` 

[](../../../common/parameters/parameters-sk.md ':include')

PersonBankruptcyProceedings
> **Príklad volania:** ```https://www.finstat.sk/api/PersonBankruptcyProceedings?name=peter&surname=toth&dateofbirth=1988-08-16&apiKey=YourAPIKey&hash=b1f071914dc48db219c7865a057e4a72d1dd6a60b919eeda3ac475a9ac7a45c4&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede
[](../../../common/responses/bankruptcyrestructuring-sk.md ':include')

[](../../../common/responses/address-sk.md ':include')

[](../../../common/responses/fulladdress-sk.md ':include')

[](../../../common/responses/personaddress-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
[](../../../common/examples/bankruptcyrestructuring.md ':include')
