##### Spoločné extended parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **Phones** | zoznam telefónnych čísel `string` – môže byť prázdny |
| **Emails** | zoznam emailov `string` – môže byť prázdny |
| **EmployeeCode** | kód počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdny |
| **EmployeeText** | textové vyjadrenie počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdne |
| **OwnershipTypeCode** | druh vlastníctva kód (číselník podľa štatistického úradu) - môže byť  prázdny |
| **OwnershipTypeText** | druh vlastníctva popis - môže byť prázdny |
| **ActualYear** | rok finančných dát (všetky {typ}Prev sú za predchádzajúci rok aktuálnemu roku) - môže byť prázdny a vtedy aj všetky ostatné finančné dáta nemajú žiadnu hodnotu, preto je vhodné používať túto položku na zisťovanie dostupnosti finančných dát |
| **CreditScoreValue** | numerické vyjadrenie hodnoty credit scoringu – môže byť prázdna |
| **CreditScoreState** | textové vyjadrenie hodnoty credit scoringu [`CreditScoreState`](#CreditScoreState) – môže byť prázdna |
| **BasicCapital** | základné imanie |
| **ProfitActual** | zisk za aktuálny rok – môže byť prázdny |
| **ProfitPrev** | zisk za aktuálny rok – môže byť prázdny |
| **RevenueActual** | suma celkových výnosov za aktuálny rok – môže byť prázdna |
| **RevenuePrev** | zisk za predchádzajúci rok – môže byť prázdny |
| **ForeignResources** | pomer cudzích zdrojov za aktuálny rok – môže byť prázdny |
| **GrossMargin** | hrubá marža za aktuálny rok – môže byť prázdna |
| **ROA** | ROA výnosov za aktuálny rok – môže byť prázdna |
| **Debts** | zoznam dlhov [`Debt`](#Debt) – môže byť prázdny |
| **StateReceivables** | zoznam pohľadávok [`ReceivableDebt`](#ReceivableDebt) |
| **CommercialReceivables** | Zoznam komerčných pohľadávok [`ReceivableDebt`](#ReceivableDebt) |
| **PaymentOrders** | zoznam platobných rozkazov [`PaymentOrder`](#PaymentOrder) |
| **WarningKaR** | posledný dátum zmeny v Konkurzoch a Reštrukturalizáciach (detaily je možné zistiť na linke WarningUrl) vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny|
| **WarningLiquidation** | posledný dátum zmeny v Likvidáciach (detaily je možné zistiť na linke WarningUrl) vo formáte `RRRR-MM-DDTHH:MM:SS`– môže byť prázdny |
| **HasDisposal** | príznak, či firma je v likvidácii `true/false` |
| **DisposalUrl** | url na likvididácie firmy |
| **SelfEmployed** | príznak, či je subjekt živnostník `true/false` |
| **Offices** | zoznam pobočiek [`Office`](#Office) – môže byť prázdny |
| **Subjects** | zoznam predmetov podnikania [`Subject`](#Subject) – môže byť prázdny |
| **ContactSources** | zoznam zdrojov jednotlivých kontaktov (položky Emails, Phones) [`ContactSource`](#ContactSource) – môže byť prázdny |
| **StructuredName** | len pri živnostníkoch, inak nie je hodnota dostupná - obsahuje rozdelený obchodný názov na jednotlivé časti [`StructuredName`](#StructuredName) |
| **JudgementFinstatLink** | odkaz na súdne rozhodnutia, ak existujú |
| **JudgementCounts** | zoznam počtov súdnych rozhodnutí [`JudgementCount`](#JudgementCount) – môže byť prázdny |
| **JudgementLastPublishedDate** | Dátum posledného súdneho rozhodnutia |
| **Ratios** | zoznam finančných ukazovateľov za posledné 4 roky [`Ratio`](#Ratio) |
| **SalesCategory** | kategória obratu |
| **CreditScoreValueIndex05** | numerické vyjadrenie hodnoty Index05 credit scoringu – môže byť prázdne |
| **CreditScoreStateIndex05** | textové vyjadrenie hodnoty Index05 credit scoringu [`CreditScoreState`](#CreditScoreState) – môže byť prázdna |
| **DistraintsAuthorization** | informácia o aktívnych povereniach na vykonanie exekúcii pre povinného [`DistraintsAuthorizationInfo`](#DistraintsAuthorizationInfo) |
| **CreditScoreValueFinStatScore** | numerické vyjadrenie hodnoty kreditného modelu FinStat skóre v percentách - može byť prázdne |
| **CreditScoreStateFinStatScore** | textové vyjadrenie hodnoty kreditného modelu FinStat skóre [`CreditScoreState`](#CreditScoreState) – môže byť prázdna |