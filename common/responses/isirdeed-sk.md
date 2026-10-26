#### IsirProceeding
Aktívne insolvenčné konanie z insolvenčného registra (ISIR), v ktorom je subjekt dlžníkom.

| Parameter | Popis |
| ----------- | ----------- |
| **FileReference** | spisová značka |
| **Url** | odkaz na detail konania |
| **Court** | kód insolvenčného súdu z ISIR (napr. `KSJIMBM`) – môže byť prázdny |
| **CourtName** | názov insolvenčného súdu – môže byť prázdny |
| **FirstEvent** | dátum prvej udalosti v konaní vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **LastEvent** | dátum poslednej udalosti v konaní vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **Status** | kód aktuálneho stavu konania [`IsirStatus`](#IsirStatus) |
| **StatusText** | popis aktuálneho stavu konania. Pri novom stave, ktorý ešte nemá kód (`Status` = `Unknown`), obsahuje pôvodný kód z ISIR |
| **Debtors** | zoznam dlžníkov [`IsirParty`](#IsirParty) |
| **Type** <i data-tier="ultimate"></i> | spôsob riešenia úpadku: `Bankruptcy` (konkurz), `Reorganization` (reorganizácia), `DebtRelief` (oddlženie). Prázdny, kým nie je vyhlásený konkurz alebo povolená reorganizácia či oddlženie |
| **TypeText** <i data-tier="ultimate"></i> | popis spôsobu riešenia – môže byť prázdny |
| **StartDate** <i data-tier="ultimate"></i> | dátum vyhlásenia konkurzu alebo povolenia reorganizácie či oddlženia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Officers** <i data-tier="ultimate"></i> | insolvenční správcovia [`IsirParty`](#IsirParty) |
| **CreditorsCount** <i data-tier="ultimate"></i> | počet veriteľov v konaní |
| **Creditors** <i data-tier="ultimate"></i> | zoznam veriteľov podľa ISIR [`IsirParty`](#IsirParty) |
| **AmountOfClaims** <i data-tier="ultimate"></i> | celková výška prihlásených pohľadávok v konaní v CZK, bez odmietnutých prihlášok. Prázdny, ak v konaní nie je žiadna prihláška; `0`, ak sú všetky odmietnuté alebo bez sumy |
| **ReceivableApplications** <i data-tier="ultimate"></i> | zoznam prihlášok pohľadávok [`ReceivableApplication`](#ReceivableApplication) – môže byť prázdny |

<span data-tier="ultimate">Veritelia v `Creditors` sú priamo z údajov ISIR, veritelia v `ReceivableApplications` z jednotlivých prihlášok, preto sa môžu líšiť.</span>

#### IsirParty
Osoba v insolvenčnom konaní (dlžník<span data-tier="ultimate">, veriteľ, správca, zástupca</span>). Firma má vyplnené `Ico`, fyzická osoba `BirthDate`, živnostník má `Ico` a môže mať aj `BirthDate`.

| Parameter | Popis |
| ----------- | ----------- |
| **Name** | názov firmy alebo meno osoby |
| **Ico** | IČO – môže byť prázdne |
| **BirthDate** | dátum narodenia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
