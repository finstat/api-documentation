#### ProceedingResult
| Parameter | Popis |
| ----------- | ----------- |
| **DebtorsAddress** | Zoznam adries dlžníkov, úpadcov, obhajcov, záložníkov alebo povinných [`PersonAddress`](#PersonAddress). Záleží od typu udalosti.|
| **ProposersAddress** | Zoznam adries navrhovateľov, resp. oprávnených [`PersonAddress`](#PersonAddress). Záleží od typu udalosti. |
| **AdministratorsAddress** | Zoznam adries správcov alebo veriteľov [`AdministratorAddress`](#AdministratorAddress) |
| **CourtsAddress** | Adresa súdu ak bola dostupná [`FullAddress`](#FullAddress) |
| **ReferenceFileNumber** | Referenčné číslo spisu na súde, typ záložného práva, typ vyrovnania, druh oznámenia, typ OV podania, spisová značka poverenia |
| **Character** | Povaha rozhodnutia |
| **Status** | Stav konania |
| **PublishDate** | Dátum zverejnenia danej udalosti (vo výnimočných prípadoch môže byť dočasne prázdna hodnota) |
| **Deadline** | Posledná lehota konania |
| **Type** |Typ udalosti. <ul><li>LawSuit – súdne rozhodnutie</li><li>PaymentOrder – platobný príkaz</li><li>Lien - záložné právo</li><li>Settlement - vyrovnanie</li><li>Notice - oznámenie</li><li>Bankruptcy - konkurzy</li><li>Restoration - reštrukturalizácie </li><li>Other - iné</li><li>DistraintsAuthorizations – poverenie na vykonanie exekúcie</li></ul> |
| **EndReason** | Dôvod ukončenia alebo zrušenia konkurzu, reštrukturalizácie, oznámenia, konania. Záleží od typu udalosti  |
| **EndStatus** | Konečný stav konania |
| **Url** | URL pre zobrazenie detailu danej udalost |
| **IssuedBy** | Informácia o tom kto konanie vydal [`IssuedPerson`](#IssuedPerson) |
| **PostedBy** | Informácia kto konanie odoslal ak je dostupná |
| **FileIdentifierNumber** | Zoznam ICS konania ak sú dostupné, číslo poverenia |