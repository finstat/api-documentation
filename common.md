# Všeobecné informácie
## O API
### Hlavná funkcionalita 
**FinStat API** slúži na získavanie informácií z portálu [FinStat.sk](https://www.finstat.sk) 
za účelom ích ďaľšieho spracovania spracovania v zákazníckych systémoch alebo stránkach.

Pre rôzne účely použitia máme definovaných viacero balíčkov API služieb.

> K používaniu API je nutné požiadať o pridelenie unikátneho API kľúča. Kontaktujte obchodné 
oddelenie na: ```info@finstat.sk```

> **Upozornenie:** Jednotlivé API balíčky sa môžu rozširovať o nové parametre, preto používajte 
spôsoby práce s API (parsre), ktoré nie sú citlivé na rozširovanie štruktúr odpoved

> Pre objednávku vyššej verzie balíčka, alebo prejednanie rozšírenia služby o nové 
parametre/údaje, kontaktujte svojho obchodníka alebo ```info@finstat.sk```


### API Limity
Prístup k API je obmedzený počtom requestov:
- Maximálny denný počet: 10 000 requestov
- Maximálny mesačný počet: 75 000 requestov

Počet maximálnych a aktuálne vyčerpaných denných limitov je možné zistiť v hlavičke každého 
response, viď príklad:

``` http
HTTP/1.1 200 OK
Cache-Control: private
Content-Type: text/xml; charset=utf-8
Server: Microsoft-IIS/8.0
X-AspNetMvc-Version: 5.2

//Limity
Finstat-Daily-Limit-Current: 1
Finstat-Daily-Limit-Max: 4000
Finstat-Monthly-Limit-Current: 241
Finstat-Monthly-Limit-Max: 75000

X-AspNet-Version: 4.0.30319
X-Powered-By: ASP.NET
Date: Tue, 22 Sep 2015 13:57:38 GMT
Content-Length: 8437
```

> **Poznámka:** v prípade prekročenia limitov sa budú requesty nad limit zarátavať ďalej. 
V prípade nechceného prekročenia limitov, napríklad z dôvodu chyby v kóde, je možné požiadať 
o ich reset (teda zníženie na nižšiu hodnotu

### Fair Use Policy
Odporúčaný počet súbežných vlákien (threadov) je **2**. Krátkodobo je vyšší počet možný, môžete 
sa však vystaviť riziku automatického zablokovania IP adresy (v prípade detekcie veľkej záťaže).

API je dostupné počas celého dňa. Treba ale rátať s tým, že v dobe špičky môže byť odpoveď 
servera dlhšia, ako je jeho odpoveď v nočných hodinách.
### Podpora JSON

Pre možnosť vrátiť odpoveď API vo formáte JSON použite jeden z nasledujúcich prepínačov:
- Pošlite v URL požiadavke parameter: ```json=true``` 
<br />Napríklad: ```https://www.finstat.sk/api/detail?json.true```
- Zakončite URL požiadavku príponou: ```.json```
<br />Napríklad: ```https://www.finstat.sk/api/detail.json```

### Podmienky využívania
FinStat API bolo vytvorené, aby bolo možné jednoducho prenášať údaje medzi FinStat servermi 
a Vašou aplikáciou. Kvôli bezpečnostným rizikám a zamedzeniu nadbytočným API volaniam, 
neimplementujte svojho klienta formou, ktorou by ste zverejnili svoje prístupové kľúče tretím 
stranám alebo by mohlo dochádzalo k častému nežiadanému volaniu. 

Nevhodnou implementáciou je napríklad vytvorenie javas-criptového klienta, ktorý by volal API 
priamo z prehliadača užívateľa. Vystavujete sa riziku, že Vaše prístupové údaje budú zneužité 
alebo sa vám vyčerpajú limity volania API.

Na volanie si vždy vytvorte medzičlánok (middleware), cez ktorý bude celá komunikácia 
prebiehať. V ňom si implementujete správne vypočítanie hashovacích reťazcov a správnu 
komunikáciu API s Vašou aplikáciou.

Môžete použiť aj niektoré z našich príkladových riešení.

## Všeobecný opis výpočtu Hash funkcie
Účelom hash funkcie je overiť požiadavku zákazníka pomocou hash funkcie, do ktorej vstupuje 
API kľúč a jeden z parametrov funkcie. 
> **Poznámka:** Pri každej definícii požiadavky je špecifikované, aký parameter sa používa na 
generovanie hash hodnoty.

### Vypočet Hash funkcie
1. Vytvorenie základnej hodnoty pre výpočet hash s hash salt, 
základ je `SomeSalt+{0}+{1}++{2}+ended` kde:
    - *{0}* – je hodnota API klúča
    - *{1}* – je hodnota privátneho (súkromného) API kľúča
    - *{2}* – je hodnota parametra funkcie (viď **Hash parameter** pri špecifikácii každej 
požiadavky)
2. Pre hashovanie je použité hashovanie SHA256, vo väčšine prípadov je nutné základnú 
hodnotu konvertovať na pole byte hodnôt, s ktorým už SHA256 knižnica vie pracovať 
(každý znak zo základnej hodnoty prevedieme na jeho byte reprezentáciu).
3. Výpočet hash hodnoty pomocou hashovacej funkcie SHA256 to poľa byte-ov.
4. Konverzia poľa byte hodnôt na textovú podobu tak, že každú hodnotu v poli prevedieme 
na dvojmiestny HEX formát, teda 0 => "00", 255 =>"FF".
5. Spojenie všetkých konvertovaných textových hodnôt do jednej hodnoty

### Príklady
#### C#
[](common/csharp.md ':include')
#### PHP
[](common/php.md ':include')
#### Java
[](common/java.md ':include')
#### Visual Basic
[](common/vbasic.md ':include')
#### Visual Basic for Applications
[](common/vba.md ':include')