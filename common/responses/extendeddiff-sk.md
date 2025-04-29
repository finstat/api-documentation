##### Spoločné diff parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **Ico**| identifikačné číslo organizácie (IČO) |
| **Dic**| daňové identifikačné číslo (DIČ) – môže byť prázdny |
| **IcDPH**| identifikačné číslo pre daň (IČ DPH) – môže byť prázdny |
| **Name**| názov firmy – môže byť prázdny |
| **Street**| ulica sídla firmy – môže byť prázdny |
| **StreetNumber**| číslo ulice sídla firmy – môže byť prázdny |
| **ZipCode**| poštové smerovacie číslo sídla firmy – môže byť prázdny |
| **City**| obec sídla firmy – môže byť prázdny |
| **District**| okres sídla firmy – môže byť prázdny |
| **Region**| kraj sídla firmy – môže byť prázdny |
| **Url**| odkaz na firmu na www.finstat.sk |
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>pre s.r.o. v tvare: Obchodný register XXXX súdu XXXXX, oddiel: xxx, vložka č.xxxx/x</li><li>pre živnostníka: Okresný úrad XXXXX, Číslo živnostenského registra: xxx-xxxx</li></ul>|
| **Activity** | odvetvie podľa FinStat kategorizácie - može byť prázdne |
| **Created** | dátum vzniku firmy vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Cancelled** | dátum zániku firmy vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **SuspendedAsPerson** | príznak či má osoba pozastavenú živnosť (`true/false`) |
| **IcDphAdditional** | detail IČ DPH pre detailné informácie o DPH [`IcDphAdditionalData`](#IcDphAdditionalData) – môže byť prázdny |
| **Warning** | príznak, či sa daná firma nachádza v zozname dlžníkov, má pohľadávku, konkurz (resp. oddlženie), poverenie na vykonanie exekúcie alebo likvidáciu (`true/false`) |
| **WarningUrl** | odkaz na podrobné informácie o rizikovej udalosti – môže byť prázdny |
| **PaymentOrderWarning** | príznak, či bol pre danú firmu vydaný platobný rozkaz (`true/false`) |
| **PaymentOrderUrl** | odkaz na podrobné informácie so zoznamom platobných rozkazov danej firmy – môže byť prázdny |
| **OrChange** | príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down) |
| **OrChangeUrl** | odkaz na podrobné informácie so zoznamom OR podaní danej firmy – môže byť prázdny |
| **SkNaceCode** | SK Nace kód – môže byť prázdny |
| **SkNaceText** | SK Nace popis – môže byť prázdny |
| **SkNaceDivision** | divízia SK Nace – môže byť prázdna |
| **SkNaceGroup** | skupina SK Nace – môže byť prázdna |
| **LegalFormCode** | právna forma kód (číselník podľa Štatistického úradu) - môže byť prázdny |
| **LegalFormText** | právna forma popis - môže byť prázdny |
| **Phones** | zoznam telefónnych čísel `string` – môže byť prázdny |
| **Emails** | zoznam emailov `string` – môže byť prázdny |
| **EmployeeCode** | kód počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdny |
| **EmployeeText** | textové vyjadrenie počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdne |
| **OwnershipTypeCode** | druh vlastníctva kód (číselník podľa štatistického úradu) - môže byť  prázdny |
| **OwnershipTypeText** | druh vlastníctva popis - môže byť prázdny |
| **ActualYear** | rok finančných dát (všetky {typ}Prev sú za predchádzajúci rok aktuálnemu roku) - môže byť prázdny a vtedy aj všetky ostatné finančné dáta nemajú žiadnu hodnotu, preto je vhodné používať túto položku na zisťovanie dostupnosti finančných dát |
| **CreditScoreValue** | numerické vyjadrenie hodnoty credit scoringu – môže byť prázdna |
| **CreditScoreState** | textové vyjadrenie hodnoty credit scoringu [`CreditScoreState`](#CreditScoreState) – môže byť prázdna |
| **ProfitActual** | zisk za aktuálny rok – môže byť prázdny |
| **ProfitPrev** | zisk za aktuálny rok – môže byť prázdny |
| **RevenueActual** | suma celkových výnosov za aktuálny rok – môže byť prázdna |
| **RevenuePrev** | zisk za predchádzajúci rok – môže byť prázdny |
| **ForeignResources** | pomer cudzích zdrojov za aktuálny rok – môže byť prázdny |
| **GrossMargin** | hrubá marža za aktuálny rok – môže byť prázdna |
| **ROA** | ROA výnosov za aktuálny rok – môže byť prázdna |
| **Debts** | zoznam dlhov [`Debt`](#Debt) – môže byť prázdny |
| **PaymentOrders** | zoznam platobných rozkazov [`PaymentOrder`](#PaymentOrder) |
| **WarningKaR** | posledný dátum zmeny v Konkurzoch a Reštrukturalizáciach (detaily je možné zistiť na linke WarningUrl) vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny|
| **WarningLiquidation** | posledný dátum zmeny v Likvidáciach (detaily je možné zistiť na linke WarningUrl) vo formáte `RRRR-MM-DDTHH:MM:SS`– môže byť prázdny |