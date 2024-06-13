# AutoLogin API

---
## Požiadavka autologin
API aktuálne poskytuje len jeden typ požiadavky, vytvorenie URL adresy s automatickým 
prihlásenim na daný účet. Návratová adresa má platnosť 10 minút a po použití linky po vypršaní 
platnosti, bude užívateľ presmerovaný na prihlasovací formulár

> **Dopytovaná URL**: ```https://cz.finstat.sk/api/autologin```<br />
> **Dopytovaná URL**: ```https://www.finstat.cz/api/autologin```<br />
> **Hash parameter**: autologin
### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **url**<br />*[povinný]*| Platná FinStat URL, na ktorú má byť užívateľ presmerovaný |
| **email**<br />*[nepovinný]*| Ak parameter nie je zadaný, užívateľ bude prihlásený pod účtom majiteľa API licencie, ktorý link vytvoril. Ak je parameter zadaný. Email musí byť prihlasovací email užívateľa, ktorý patrí do podlicencií majiteľa API. Inak vráti chybu |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/autologin?url=https://finstat.sk/35757442&email=email@domena.tldapikey=YourAPIKey&hash=cdab830acd61becad8aa9a7c501f68a9e8e03c37103e4ac52a4d0209d39781f5&StationId=YourStationID&StationName=Your+Station+Name```

### Popis odpovede

Odpoveď pozostáva z jendého elementu obsahujúceho autologin link na vami zadanú url.


#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

### Príklad XML odpovede
Príklad XML odpovede (na url `https://finstat.sk/35757442`):

[](../../../common/examples/autologin.md ':include')