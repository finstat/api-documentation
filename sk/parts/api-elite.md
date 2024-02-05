##### Spoločné extended parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **Phones** | zoznam telefónnych čísel – null, alebo pole hodnôt |
| **Emails** | zoznam emailov – null, alebo pole hodnôt |
| **EmployeeCode** | kód počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdny |
| **EmployeeText** | textové vyjadrenie počtu zamestnancov podľa metodiky štatistického úradu – môže byť prázdne |
| **OwnershipTypeCode** | druh vlastníctva kód (číselník podľa štatistického úradu) - môže byť  prázdny |
| **OwnershipTypeText** | druh vlastníctva popis - môže byť prázdny |
| **ActualYear** | rok finančných dát (všetky {typ}Prev sú za predchádzajúci rok aktuálnemu roku) - môže byť prázdny a vtedy aj všetky ostatné finančné dáta nemajú žiadnu hodnotu, preto je vhodné používať túto položku na zisťovanie dostupnosti finančných dát |
| **CreditScoreValue** | numerické vyjadrenie hodnoty credit scoringu – môže byť prázdna |
| **CreditScoreState** | textové vyjadrenie hodnoty credit scoringu – môže byť prázdna, kde:<ul><li>Red – vysoká pravdepodobnosť úpadku</li><li>Yellow – pásmo šedej zóny</li><li>Green – finančne stabilná spoločnosť</li></ul> |
| **BasicCapital** | Základné imanie |
| **ProfitActual** | zisk za aktuálny rok – môže byť prázdny |
| **ProfitPrev** | zisk za aktuálny rok – môže byť prázdny |
| **RevenueActual** | suma celkových výnosov za aktuálny rok – môže byť prázdna |
| **RevenuePrev** | zisk za predchádzajúci rok – môže byť prázdny |
| **ForeignResources** | pomer cudzích zdrojov za aktuálny rok – môže byť prázdny |
| **GrossMargin** | hrubá marža za aktuálny rok – môže byť prázdna |
| **ROA** | ROA výnosov za aktuálny rok – môže byť prázdna |
| **Debts** | zoznam dlhov (null ak nie je žiaden dlh, alebo obsahuje viac elementov `Dept`)<table><tr><td>Source</td><td>typ zdroja<ul><li>Tax - daňový nedoplatok daňovému úradu</li><li>Coll - colný nedoplatok daňovému úradu</li><li>Social - dlh sociálneho poistenia</li><li>Vszp - nedoplatok preddavku poistného VSZP poistovňa</li><li>Union - nedoplatok preddavku poistného Union poistovňa</li><li>Dovera – dlh voči zdravotnej poisťovni Dôvera</ul></td></tr><tr><td>Value</td><td>hodnota dlhu</td></tr><tr><td>ValidFrom</td><td>dátum detekovania dlhu vo formáte (RRRR-MMDDTHH:MM:SS)</td></tr></table>|
| **StateReceivables** | zoznam pohľadávok. Štruktúra podobná ako pri dlhoch.<br />`StateReceivables` obsahuje jednotlivé elementy:<table><tr><td>Source</td><td>Správca</td></tr><tr><td>Value</td><td>hodnota dlhu</td></tr><tr><td>ValidFrom</td>dátum detekovania dlhu vo formáte (RRRR-MMDDTHH:MM:SS)<td></td></tr></table>|
| **CommercialReceivables** | Zoznam komerčných pohľadávok. Štruktúra podobná ako pri `StateReceivables`<br />`CommercialReceivables` obsahuje jednotlivé elementy<table><tr><td>Source</td><td>Správca</td></tr><tr><td>Value</td><td>hodnota dlhu</td></tr><tr><td>ValidFrom</td><td>dátum detekovania dlhu vo formáte (RRRR-MMDDTHH:MM:SS)</td></tr></table>|
| **PaymentOrders** | oznam platobných rozkazov (null ak nie je žiaden platobný rozkaz, alebo obsahuje viac XML elementov `PaymentOrder`)<table><tr><td>PublishDate</td><td>dátum zverejnenia</td></tr><tr><td>Value</td><td>hodnota platobného rozkazu (može byť null)</td></tr></table>|
| **WarningKaR** | posledný dátum zmeny v Konkurzoch a Reštrukturalizáciach (detaily je možné zistiť na linke WarningUrl) vo formáte (RRRR-MM-DDTHH:MM:SS) – môže byť prázdny|
| **WarningLiquidation** | posledný dátum zmeny v Likvidáciach (detaily je možné zistiť na linke WarningUrl) vo formáte (RRRR-MM-DDTHH:MM:SS)– môže byť prázdny |
| **HasDisposal** | Príznak, či firma je v likvidácii (true/false) |
| **DisposalUrl** | Url na likvididácie firmy |
| **SelfEmployed** | príznak, či je subjekt živnostní |
| **Offices** | zoznam pobočiek<table><tr><td>City</td><td>mesto</td></tr><tr><td>Country</td><td>krajina/štát</td></tr><tr><td>District</td><td>okres</td></tr><tr><td>Region</td><td>kraj</td></tr><tr><td>Street</td><td>ulica</td></tr><tr><td>StreetNumber</td><td>popisné čislo budovy</td></tr><tr><td>Subjects</td><td>zoznam predmetov podnikania</td></tr><tr><td>ZipCode</td><td>PSČ</td></tr><tr><td>Type</td><td>typ adresy</td></tr></table> |
| **Subjects** | Subjects <table><tr><td>Title</td><td>názov</td></tr><tr><td>ValidFrom</td><td>dátum zápisu</td></tr><tr><td>SuspendedFrom</td><td>dátum pozastavenia od (nemusí byť vyplnený) - iba pri aktuálne pozastavených predmetoch podnikania</td></tr><tr><td>SuspendedAsPersonTo</td><td>dátum pozastavenia do (nemusí byť vyplnený) - iba pri aktuálne pozastavených predmetoch podnikania</td></tr></table> |
| **ContactSources** | Zoznam zdrojov jednotlivých kontaktov (položky Emails, Phones)<table><tr><td>Contact</td><td>Hodnota kontaktu – email alebo telefón</td></tr><tr><td>Sources</td><td>Zoznam zdrojov kontaktu</td></tr></table> |
| **StructuredName** | Len pri živnostníkoch, inak nie je hodnota dostupná - obsahuje rozdelený obchodný názov na jednotlivé časti.<table><tr><td>Prefix</td><td>zoznam titulov pred menom</td></tr><tr><td>Name</td><td>meno (max 2 položky)</td></tr><tr><td>Suffix</td><td>zoznam titulov za menom</td></tr><tr><td>After</td><td>všetky ostatné slová za menom</td></tr></table> |
| **JudgementIndicators** | Indikátory súdnych rozhodnutí<ul><li>Defendant – odporca (true/false)</li><li>Plaintiff – navrhovateľ (true/false)</li></ul>|
| **JudgementFinstatLink** | Odkaz na súdne rozhodnutia, ak existujú |
| **JudgementCounts** | Počty jednotlivých súdnych rozhodnut<ul><li>Defendant – odporca</li><li>Plaintiff – navrhovateľ</li><li>Attorney – zástupca</li></ul> |
| **JudgementLastPublishedDate** | Dátum posledného súdneho rozhodnutia |
| **Ratios** |Finančné ukazovatele za posledné 4 roky<ul><li>Profit – Zisk</li><li>Sales – Tržby</li><li>Assets – Aktíva</li><li>Equity – Vlastný kapitál</li><li>ShareCapital – Základné imanie</li><li>EBIT – Zisk pred zaplatením dane a úrokov</li><li>EBITDA – Zisk pres zaplatenín dane, úrokov, znehodnotením a amortizáciou</li><li>ValueAddedd – Pridaná hodnota</li><li>ROE – Návratovosť kapitálu</li><li>ROA – Návratovosť Aktív</li><li>AssetsToLiabilities – Zadĺženosť</li><li>Depreciation – Odpisy</li><li>GrossMargin – Hrubá Marža</li><li>CreditScoring - Altman Z-score</li><li>CreditScoringIndex05 – INDEX 05</li></ul><table><tr><td>Year</td><td>Rok</td></tr><tr><td>Value</td><td>Hodnota</td></tr></table> |
| **SalesCategory** | Kategória obratu |
| **CreditScoreValueIndex05** | Numerické vyjadrenie hodnoty Index05 credit scoringu – môže byť prázdne |
| **CreditScoreStateIndex05** | textové vyjadrenie hodnoty Index05 credit scoringu – môže byť prázdna, <br/>kde:<ul><li>Red – vysoká pravdepodobnosť úpadku</li><li>Yellow – pásmo šedej zóny</li><li>Green – finančne stabilná spoločnosť</li></ul>|
| **DistraintsAuthorization** | Informácia o aktívnych povereniach na vykonanie exekúcii pre povinného <table><tr><td>LastPublishDate</td><td>dátum zverejnenia posledného aktívneho poverenia</td></tr><tr><td>Count</td><td>počet aktívnych poveren</td></tr></table>|
| **CreditScoreValueFinStatScore** | Numerické vyjadrenie hodnoty kreditného modelu FinStat skóre v 
percentách - može byť prázdnea |
| **CreditScoreStateFinStatScore** | textové vyjadrenie hodnoty kreditného modelu FinStat skóre – môže byť prázdna, <br />kde:<ul><li>Red – vysoká pravdepodobnosť úpadku</li><li>Yellow – pásmo šedej zóny</li><li>Green – finančne stabilná spoločnosť</li></ul>|