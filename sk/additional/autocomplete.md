# Autocomplete
Api slúži na nájdenie hodntoty IČO alebo názvu firmy podľa vyhľadávanéo reťazca

---
## Požiadavka autocomplete
Vráti nápovedy na firmy uložené v databáze FinStat.sk na základe vyhľadávaného reťazca *query*.
> **Dopytovaná URL**: ```https://www.finstat.sk/api/autocomplete```<br />
> **Hash parameter**: {query}
### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **query**<br />*[povinný]*| vyhľadávaný výraz pre autocomplete (minimálna dĺžka 3 znaky, inak je vrátený chybový stav) |

[](../parts/parameters.md ':include')


> **Príklad volania:** ```https://www.finstat.sk/api/autocomplete?query=test&apikey=YourAPIKey&hash=63678854b4b02034b4127cd9188b3a514b67e054465e3b8d4dd5284c46f7c099&StationId=YourStationID&StationName=Your+Station+Name```
### Popis odpovede

Popis jednotlivých XML elementov:

| Parameter | Popis |
| ----------- | ----------- |
| **Results** | zoznam firiem, ktoré vyhovujú zadanému query výrazu (prvých 20 výsledkov).<br/>Element Company obsahuje jednotlivé elementy:<table><tr><td>Ico</td><td>IČO firmy</td></tr><tr><td>Name</td><td>meno firmy</td></tr><tr><td>City</td><td>mesto sídla firmy</td></tr><tr><td>Cancelled </td><td>informácia, či bola firma zrušená (hodnoty true/false)</td></tr></table>|
| **Suggestions** | Pole hodnôt návrhov správneho výrazu pre autocomplete (prvých 10 výrazov) |


#### Návratové HTTP error kódy:
| Error kód | Popis |
| ----------- | ----------- |
| **404**| špecifikovaný query výraz je príliš krátky (minimálna dĺžka 3 znaky) |

[](../parts/httperrorcodes.md ':include')

### Príklad XML odpovede
Príklad XML odpovede (na query `test`):

[](../../examples/autocomplete.md ':include')

