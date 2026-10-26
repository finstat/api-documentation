#### Jazyk požiadavky
| Parameter | Popis |
| ----------- | ----------- |
| **lang**<br />*[nepovinný]*| jazyk popisov v odpovedi: `sk` alebo `cs`. Platí iba pre `www.finstat.cz`, na `cz.finstat.sk` sú popisy po slovensky (Free, Detail a PremiumCZ tam dočasne, do vydania nového CZ API, vracajú `LegalForm`, `OwnershipType` a popisy CZ NACE po česky). Ak chýba, použije sa jazyk z hlavičky `Accept-Language`, inak čeština. Nie je súčasťou hashu. Jazyk odpovede vracia hlavička `Content-Language` |
