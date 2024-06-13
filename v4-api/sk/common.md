# O API

Táto technická dokumentácia Vám pomôže vyhľadať a získať údaje o firmách pomocou V4 API. 
Základné údaje:
- FinStat V4 API je postavené pomocou služby Azure API Management 
- Výstupné dáta sú vo formáte .JSON

## Dostupné krajiny
FinStat V4 API momentálne pokrýva údaje o firmách z nasledujúcich krajín:
- Slovenská republika (sk)
- Česká republika (cz)
- Poľsko (pl)
- Maďarsko (hu)
- Rakúsko (at)
- Nemecko (de)
- Veľká Británia (gb)
- Francúzsko (fr)
- Lotyšsko (lv)
- Estónsko (ee)

## Ako začať

Na získanie API kľúčov kontaktujte prosím FinStat team na `info@finstat.sk`. Poskytujeme aj časovo 
obmedzené testovacie prístupy, aby ste si mohli vyskúšať rozhranie a vyhodnotiť obsah API.

Získate prístup na developerský portál Azure API Management, kde nájdete popis API vrátane 
testovacieho rozhrania.
Prihlásiť sa na developerský portál môžete na [https://hithorizonsapim.portal.azure-api.net/](https://hithorizonsapim.portal.azure-api.net/).

## Podmienky používania a limity

Základné pravidlá používania:
- API je dostupné na nasledovnej adrese: `https://api.hithorizons.com/invoicing/{COUNTRY_CODE}/`
    - COUNTRY_CODE je potrebné nahradiť 2-písmenovým ISO kódom dopytovanej krajiny, a teda napríklad de pre Nemecko, pl pre Poľsko.
- Všetky dopyty musia byť autentifikované API kľúčom. API kľúč je posielaný v http headeri  `Ocp-Apim-Subscription-Key`.
- Dáta v odpovedi obsahujú nasledovné polia:
    - Success [bool]: indikuje, či bolo volanie úspešné 
    - Error [string]: v prípade chyby obsahuje popis chyby 
    - Result: dopytované dáta
-  Limity na počet volaní:
    -  30 volaní/min
    -  denný limit v testovacej verzii: 300/deň
    -  denný limit: 1000
    -  mesačný limit: 10000

### Odpoveď po prekročení minútového limitu
Po prekročení 30 volaní na minútu sa vráti nasledovná odpoveď
``` http
HTTP/1.1 429 Too Many Requests
Content-Length: 84
Content-Type: application/json
Retry-After: 12
{
    "statusCode": 429,
    "message": "Rate limit is exceeded. Try again in 12 seconds."
}
```

Odpoveď indikuje, že klient nemá prístup k API po dobu uvedenú v headeri `Retry-After` (v sekundách). 
Textový popis problému sa vráti v `message` poli odpovede.
Po prijatí odpovede bude `message` zobrazená používateľovi. Nasledujúce volania budú úspešné až po 
uplynutí doby uvedenej v `Retry-after`

### Odpoveď po prekročení denného a mesačného limitu

Po prekročení denného a mesačného limitu sa zobrazí odpoveď
``` http
HTTP/1.1 403 Quota Exceeded (Daily)
Content-Length: 551
{
    "statusCode": 403,
    "message": "You have exceeded your HitHorizons daily API quota.",
    "linkText": "Ask for a higher quota »",
    "link": "https://www.hithorizons.com/services/api/api-daily-quotaexceeded",
    "popupTitle": "HitHorizons API quota exceeded",
    "popupMessage": "You have exceeded your daily API quota: 20 000 requests.\n\nGet the higher API quota for continuous work with the European companies' data withi {integrationName}.",
    "popupLinkText": "Inquire now",
    "popupLink": "https://www.hithorizons.com/services/api/api-daily-quotaexceeded",
    "subscriptionid": "5efa324543fd361210d2e76a"  
}
```

- Kód statusu je 403 (Forbidden)
- Správa statusu indikuje prekročenie limitu. Správa vždy začína s `"Quota Exceeded“` s doplňujúcimi informáciami o type prekročeného limitu:
    -  Quota Exceeded (Daily) 
    -  Quota Exceeded (Monthly)
    -  Quota Exceeded (Daily Trial)
- Telo odpovede pozostáva z nasledovných polí:
    - `statusCode`: 403
    - `message`: správa zobrazená používateľovi
    - `linkText`: značka, link alebo button vedľa správy
    - `link`: cieľová URL po kliknutí na odkaz/button s vyššie uvedeným označením
    - `popupTitle`: nadpis okna popupu
    - `popupMessage`: správa, ktorá sa zobrazí v popoup okne
    - `popupLinkText`: značka, link alebo button na zobrazenie vedľa správy v popup okne
    - `popupLink`: cieľová URL po kliknutí na link/button v popup okne so značkou hore
    - `suscriptionId`: ID predplatného, ktoré môže byť použité na identifikáciu zákazníckeho konta
- Texty môžu obsahovať placeholder {integrationName}, ktorý by mal byť nahradený softvérom, v ktorom je V4 API integrované, napríklad Dynamics 365. 
- Texty môžu obsahovať znaky nového riadku (`\n`), ktré by mali byť interpretované ako nové riadky.
- Vrátené správy sú relevantné k prekročeniu limitov. Sú rôzne pre denný/mesačný limit, ako aj pre info o expirovaní licencie.
- Štruktúra tela objektu bude vždy taká, aká je tu popísaná.

Po obdržaní takejto odpovede bude `message` a `linkText` zobrazený používateľovi, pričom `linkText`
bude zobrazený ako hyperlink stránky v `link`.

`popupMessage` s `popupTitle` bude zobrazená používateľovi hneď po prekročení limitu. `popupLinkText`
slúži ako button na popup okne a súvisí s `popupLink.`
