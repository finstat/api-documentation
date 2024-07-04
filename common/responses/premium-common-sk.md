##### Spoločné detail parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **RegisterNumberText** | textový popis registračných údajov – môže byť prázdny <ul><li>pre s.r.o. v tvare: Zapísaná na Okr. súde XXXXX, odd. Sro, vl.č.xxxx/L</li><li>pre živnostníka: Číslo živn.registra: xxx-xxxx, okresný úrad XXXXX </li></ul>|
| **Activity** | odvetvie podľa FinStat kategorizácie - može byť prázdne |
| **Created** | dátum vzniku firmy vo formáte `RRRR-MMTDDTHH:MM:SS` – môže byť prázdny |
| **Cancelled** | dátum zániku firmy vo formáte `RRRR-MMTDDTHH:MM:SS` – môže byť prázdny |
| **SuspendedAsPerson** | príznak či má osoba pozastavenú živnosť (`true/false`) |
| **IcDphAdditional** | detail IČ DPH pre detailné informácie o DPH [`IcDphAdditional`](#IcDphAdditional) – môže byť prázdny |
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
| **RpvsInsert** | indikácia, či je firma aktuálne zapísaná v RPVS/ číslo vložky – môže byť prázdny |
| **RpvsUrl** | odkaz na záložku Osoby vo firme na portáli FinStat.sk – môže byť prázdny |
| **ProfitActual** | zisk za aktuálny rok – môže byť prázdny |
| **RevenueActual** | suma celkových výnosov za aktuálny rok – môže byť prázdna |
| **JudgementIndicators** | zoznam indikátorov súdnych rozhodnutí [`JudgementIndicator`](#JudgementIndicator) – môže byť prázdny|
| **JudgementFinstatLink** | odkaz na súdne rozhodnutia, ak existujú – môže byť prázdny |
| **SalesCategory** | kategória obratu – môže byť prázdny |
| **HasKaR** | Príznak, či firma má konkurz alebo reštrukturalizáciu (`true/false`) |
| **KarUrl** | Url na zoznam konkurzov a reštrukturalizácií firmy – môže byť prázdny |
| **HasDebt** | Príznak, či firma má aktuálny dlh, pohľadávku štátu alebo komerčnú pohľadávku (`true/false`) |
| **DebtUrl** | Url na zoznam dlhov a pohľadávok firmy – môže byť prázdny |
| **BankAccounts** | Zoznam  aktuálne nahlásených účtov na Finančnej správe [`BankAccount`](#BankAccount) – môže byť prázdny |
| **TaxReliabilityIndex** | Index daňovej spoľahlivosti. Môže byť prázdny.<br/>Hodnoty:<ul><li>vysoko spoľahlivý</li><li>spoľahlivý</li><li>menej spoľahlivý</li><li>nehodnotený</li></ul>|
| **SuspendedAsPersonUntil** | pri živnostníkoch - vyplnený len v tom prípade,ak má živnosť pozastavené všetky predmety podnikania - vtedy sa vyberie ten najskorší termín |