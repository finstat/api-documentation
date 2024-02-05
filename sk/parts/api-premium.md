##### Spoločné detail parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>pre s.r.o. v tvare: Zapísaná na Okr. súde XXXXX, odd. Sro, vl.č.xxxx/L</li><li>pre živnostníka: Číslo živn.registra: xxx-xxxx, okresný úrad XXXXX </li></ul>|
| **Activity** | odvetvie podľa FinStat kategorizácie - može byť prázdne |
| **Created** | dátum vzniku firmy vo formáte (RRRR-MM-DDTHH:MM:SS) – môže byť prázdny |
| **Cancelled** | dátum zániku firmy vo formáte (RRRR-MM-DDTHH:MM:SS) – môže byť prázdny |
| **SuspendedAsPerson** | príznak či má osoba pozastavenú živnosť (true/false) |
| **IcDphAdditional** | detail IČ DPH pre detailné informácie o DPH – môže byť prázdny<br/>`IcDphAdditional` obsahuje jednotlivé elementy:<table><tr><td>IcDph</td><td>číslo IČ DPH aj v prípade, ak firma je v zozname vymazaných subjektov</td></tr><tr><td>Paragraph</td><td>paragraf, pre ktorý je číslo DPH vydané aj v prípade, že firma je v zozname vymazaných subjektov</td></tr><tr><td>CancelListDetectedDate</td><td>dátum detekovania firmy v zozname subjektov s dôvodom na zrušenie DPH (RRRR-MM-DDTHH:MM:SS) – môže byť prázdny</td></tr><tr><td>RemoveListDetectedDate</td><td>dátum detekovania firmy v zozname subjektov Zoznam vymazaných platiteľov DPH podľa §52 ods.8 zákona 563/2009 Z. z. (RRRR-MM-DDTHH:MM:SS) – môže byť prázdny</td></tr></table> |
| **Warning** | príznak, či sa daná firma nachádza v zozname dlžníkov, má pohľadávku, konkurz (resp. oddlženie), poverenie na vykonanie exekúcie alebo likvidáciu (true/false) |
| **WarningUrl** | odkaz na podrobné informácie o rizikovej udalosti – môže byť prázdny |
| **PaymentOrderWarning** | príznak, či bol pre danú firmu vydaný platobný rozkaz (true/false) |
| **PaymentOrderUrl** | odkaz na podrobné informácie so zoznamom platobných rozkazov danej firmy – môže byť prázdny |
| **OrChange** | príznak nárastu/poklesu tržieb firmy medzi posledným a predposledným rokom v databáze (Unknown, Up, Down) |
| **OrChangeUrl** | príznak nárastu/poklesu zisku firmy medzi posledným a predposledným  rokom v databáze (Unknown, Up, Down, Loss)<br />stav loss znamená, že firma vykázala za posledný rok stratu |
| **SkNaceCode** | SK Nace kód – môže byť prázdny |
| **SkNaceText** | SK Nace popis – môže byť prázdny|
| **SkNaceDivision** | divízia SK Nace – môže byť prázdna |
| **SkNaceGroup** | skupina SK Nace – môže byť prázdna |
| **LegalFormCode** | právna forma kód (číselník podľa Štatistického úradu) - môže byť prázdny |
| **LegalFormText** | právna forma popis - môže byť prázdny |
| **RpvsInsert** | indikácia, či je firma aktuálne zapísaná v RPVS/ číslo vložky – môže byť prázdny |
| **RpvsUrl** | odkaz na záložku Osoby vo firme na portáli FinStat.sk – môže byť prázdny |
| **ProfitActual** | zisk za aktuálny rok – môže byť prázdny |
| **RevenueActual** | suma celkových výnosov za aktuálny rok – môže byť prázdna |
| **JudgementIndicators** | indikátory súdnych rozhodnutí – môže byť prázdny<ul><li>Defendant – odporca (true/false)</li><li>Plaintiff – navrhovateľ (true/false)</li></ul>|
| **JudgementFinstatLink** | odkaz na súdne rozhodnutia, ak existujú – môže byť prázdny |
| **SalesCategory** | kategória obratu – môže byť prázdny |
| **HasKaR** | Príznak, či firma má konkurz alebo reštrukturalizáciu (true/false) |
| **KarUrl** | Url na zoznam konkurzov a reštrukturalizácií firmy – môže byť prázdny |
| **HasDebt** | Príznak, či firma má aktuálny dlh, pohľadávku štátu alebo komerčnú pohľadávku (true/false) |
| **DebtUrl** | Url na zoznam dlhov a pohľadávok firmy – môže byť prázdny |
| **BankAccounts** |Zoznam bankových účtov aktuálne nahlásených Finančnej správe.<br /> BankAccounts obsahuje jednotlivé elementy typu `BankAccount`:<table><tr><td>AccountNumber</td><td>Číslo účtu</td></tr><tr><td>PublishedAt</td><td>Dátum zverejnenia na Finančnej správe</td></tr></table>|
| **TaxReliabilityIndex** | Index daňovej spoľahlivosti. Môže byť prázdny.<br/>Hodnoty:<ul><li>vysoko spoľahlivý</li><li>spoľahlivý</li><li>menej spoľahlivý</li><li>nehodnotený</li></ul>|
| **SuspendedAsPersonUntil** | pri živnostníkoch - vyplnený len v tom prípade,ak má živnosť pozastavené všetky predmety podnikania - vtedy sa vyberie ten najskorší termín |