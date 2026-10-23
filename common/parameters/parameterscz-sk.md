#### Spoločné parametre API požiadavky
| Parameter | Popis |
| ----------- | ----------- |
| **apiKey**<br />*[povinný]*| unikátny kľúč pridelený každému používateľovi API |
| **hash**<br />*[povinný]*| SHA256 hash [vygenerovaný spojením viacerých parametrov a privátneho reťazca](cz-api/sk/common.md?id=všeobecný-opis-výpočtu-hash-funkcie)<br />(pre viac info ```info@finstat.sk```) |
| **stationId**<br />*[nepovinný]*| identifikácia stanice používateľa API |
| **stationName**<br />*[nepovinný]*| názov stanice používateľa API |
| **lang**<br />*[nepovinný]*| jazyk popisov v odpovedi: `sk` alebo `cs`. Platí iba pre `www.finstat.cz`, na `cz.finstat.sk` sú popisy po slovensky (Free, Detail a PremiumCZ tam dočasne, do vydania nového CZ API, vracajú `LegalForm`, `OwnershipType` a popisy CZ NACE po česky). Ak chýba, použije sa jazyk z hlavičky `Accept-Language`, inak čeština. Nie je súčasťou hashu. Jazyk odpovede vracia hlavička `Content-Language` |