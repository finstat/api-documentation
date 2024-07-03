# PremiumCZ API
API slúži na vyžiadanie detailu firmy

---
## Požiadavka detail
Výpis detailu firmy na základe parametra *ico*
> **Dopytovaná URL**: ```https://cz.finstat.sk/api/premium```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/premium```<br />
> **Hash parameter**: {ico}
### Parametre
[](../../../common/parameters/detail-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')


> **Príklad volania:** ```https://www.finstat.cz/api/premium?ico=47165367&apikey=YourAPIKey&hash=a85aff26f1d2aae0059ec051866daa6246374d65da4a2c289d9ce8cbcd73a7b5&StationId=YourStationID&StationName=Your+Station+Name```
### Popis odpovede

Dopyt vráti odpoveď s nasledulúcimi parametrami:

[](../../../common/responses/basiccz-sk.md ':include')

[](../../../common/responses/premiumcz-common-sk.md ':include')

##### Doplnené parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **VATNumber** | daňová identifikácia |
| **TaxPayer** | ozačenie či je platca DPH (true/false)|
| **LegalFormCode** | právna forma kód - môže byť prázdny |
| **OwnershipTypeCode** | druh vlastníctva kód - môže byť prázdny |
| **BankAccounts** |Zoznam bankových účtov.<br /> BankAccounts obsahuje jednotlivé elementy typu `BankAccount`:<table><tr><td>**AccountNumber**</td><td>Číslo účtu</td></tr><tr><td>**PublishedAt**</td><td>Dátum zverejnenia na Finančnej správe</td></tr></table>|
| **Uneliability** | ozačenie či je nedôverihodný platca /osoba|
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>pre s.r.o. v tvare: Zapísaná na Okr. súde XXXXX, odd. Sro, vl.č.xxxx/L</li><li>pre živnostníka: Číslo živn.registra: xxx-xxxx, okresný úrad XXXXX </li></ul>|
| **ActualYear**| rok poslednej finančnej závierky |
| **SalesActual**| hodnota tržieb za posledný dosupný rok |
| **ProfitActual**| hodnota zisku za posledný dosupný rok|
| **Sales**| príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down) |
| **Profit**| príznak nárastu/poklesu zisku firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down, Loss) stav loss znamená, že firma vykázala za posledný rok stratu |

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk-detail.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede