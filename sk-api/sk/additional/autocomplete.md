# Autocomplete
Api slúži na nájdenie hodntoty IČO alebo názvu firmy podľa vyhľadávaného reťazca

## Požiadavka autocomplete
Vráti nápovedy na firmy uložené v databáze FinStat.sk na základe vyhľadávaného reťazca *query*.
Nápovedu vráti v rámcu štruktúry [`ApiAutoComplete`](#ApiAutoComplete)
Odoslaný vyhľadávaný reťazec bude z výkonnostých dôvodov serverom automatický skrátený na prvých 100 slov.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/autocomplete```<br />
> **Hash parameter**: {query}

### Parametre
[](../../../common/parameters/autocomplete-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/autocomplete?query=test&apikey=YourAPIKey&hash=63678854b4b02034b4127cd9188b3a514b67e054465e3b8d4dd5284c46f7c099&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **404**| špecifikovaný query výraz je príliš krátky (minimálna dĺžka 3 znaky) |

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovede

[](../../../common/responses/autocomplete-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
Príklad XML odpovede (na query `test`):

[](../../../common/examples/autocomplete.md ':include')
