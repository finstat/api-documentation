# AutoLogin API

## Požiadavka autologin
API aktuálne poskytuje len jeden typ požiadavky, vytvorenie URL adresy s automatickým 
prihlásenim na daný účet. Návratová adresa má platnosť 10 minút a po použití linky po vypršaní 
platnosti, bude užívateľ presmerovaný na prihlasovací formulár.

Odpoveď pozostáva z jendého elementu obsahujúceho autologin link na vami zadanú url.

> **Dopytovaná URL**: ```https://www.finstat.sk/api/autologin```<br />
> **Hash parameter**: autologin

### Parametre
[](../../../common/parameters/autologin-sk.md ':include')

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/autologin?url=https://finstat.sk/35757442&email=email@domena.tld&apikey=YourAPIKey&hash=cdab830acd61becad8aa9a7c501f68a9e8e03c37103e4ac52a4d0209d39781f5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

# Príklad XML odpovede
Príklad XML odpovede (na url `https://finstat.sk/35757442`):

[](../../../common/examples/autologin.md ':include')