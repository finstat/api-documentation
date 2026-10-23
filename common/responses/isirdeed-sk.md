#### IsirProceeding
Aktívne insolvenčné konanie z insolvenčného registra (ISIR), v ktorom je subjekt dlžníkom. EliteCZ vracia základné údaje, UltimateCZ aj rozšírené.

| Parameter | Popis | Balík |
| ----------- | ----------- | ----------- |
| **FileReference** | spisová značka | EliteCZ |
| **Url** | odkaz na detail konania | EliteCZ |
| **Court** | kód insolvenčného súdu z ISIR (napr. `KSJIMBM`) – môže byť prázdny | EliteCZ |
| **CourtName** | názov insolvenčného súdu – môže byť prázdny | EliteCZ |
| **FirstEvent** | dátum prvej udalosti v konaní vo formáte `RRRR-MM-DDTHH:MM:SS` | EliteCZ |
| **LastEvent** | dátum poslednej udalosti v konaní vo formáte `RRRR-MM-DDTHH:MM:SS` | EliteCZ |
| **Status** | kód aktuálneho stavu konania [`IsirStatus`](#IsirStatus) | EliteCZ |
| **StatusText** | popis aktuálneho stavu konania. Pri novom stave, ktorý ešte nemá kód (`Status` = `Unknown`), obsahuje pôvodný kód z ISIR | EliteCZ |
| **Debtors** | zoznam dlžníkov [`IsirParty`](#IsirParty) | EliteCZ |
| **Type** | spôsob riešenia úpadku: `Bankruptcy` (konkurz), `Reorganization` (reorganizácia), `DebtRelief` (oddlženie). Prázdny, kým nie je vyhlásený konkurz alebo povolená reorganizácia či oddlženie | UltimateCZ |
| **TypeText** | popis spôsobu riešenia – môže byť prázdny | UltimateCZ |
| **StartDate** | dátum vyhlásenia konkurzu alebo povolenia reorganizácie či oddlženia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny | UltimateCZ |
| **Officers** | insolvenční správcovia [`IsirParty`](#IsirParty) | UltimateCZ |
| **CreditorsCount** | počet veriteľov v konaní | UltimateCZ |
| **Creditors** | zoznam veriteľov podľa ISIR [`IsirParty`](#IsirParty) | UltimateCZ |
| **AmountOfClaims** | celková výška prihlásených pohľadávok v konaní v CZK, bez odmietnutých prihlášok. Prázdny, ak v konaní nie je žiadna prihláška; `0`, ak sú všetky odmietnuté alebo bez sumy | UltimateCZ |
| **ReceivableApplications** | zoznam prihlášok pohľadávok [`ReceivableApplication`](#ReceivableApplication) – môže byť prázdny | UltimateCZ |

Veritelia v `Creditors` sú priamo z údajov ISIR, veritelia v `ReceivableApplications` z jednotlivých prihlášok, preto sa môžu líšiť.

#### IsirParty
Osoba v insolvenčnom konaní (dlžník, veriteľ, správca, zástupca). Firma má vyplnené `Ico`, fyzická osoba `BirthDate`.

| Parameter | Popis |
| ----------- | ----------- |
| **Name** | názov firmy alebo meno osoby |
| **Ico** | IČO – môže byť prázdne |
| **BirthDate** | dátum narodenia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |

#### ReceivableApplication
Jedna prihláška pohľadávok v konaní. Zodpovedá jednému riadku na webe v záložke Prihlášky pohľadávok. Jednotlivé pohľadávky z prihlášky sa nevracajú, iba ich počet a celková suma.

| Parameter | Popis |
| ----------- | ----------- |
| **Creditor** | veriteľ [`IsirParty`](#IsirParty) – môže byť prázdny, ak sa veriteľa z prihlášky nepodarilo priradiť |
| **Representative** | zástupca veriteľa [`IsirParty`](#IsirParty), iba `Name` a `Ico` – môže byť prázdny |
| **PublishDate** | dátum zverejnenia prihlášky vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **ClaimsCount** | počet pohľadávok v prihláške (na webe „Pohľadávky“) – môže byť prázdny |
| **TotalAmount** | celková suma pohľadávok v prihláške v CZK (na webe „Celková suma“) – môže byť prázdny |

#### IsirStatus
| Kód | Stav v ISIR | Popis |
| ----------- | ----------- | ----------- |
| `PendingInsolvencyDecision` | NEVYRIZENA | pred rozhodnutím o úpadku |
| `Moratorium` | MORATORIUM | povolené moratórium |
| `Insolvency` | ÚPADEK | v úpadku |
| `Bankruptcy` | KONKURS | vyhlásený konkurz |
| `DebtRelief` | ODDLUŽENÍ | povolené oddlženie |
| `Reorganization` | REORGANIZ | povolená reorganizácia |
| `Resolved` | VYRIZENA | vybavená vec |
| `AnnulledByHighCourt` | ZRUŠENO VS | zrušené vrchným súdom |
| `BankruptcyAfterAnnulment` | K-PO ZRUŠ. | vyhlásený konkurz po zrušení vrchným súdom |
| `Reopened` | OBZIVLA | obživnutá vec |
| `Transferred` | NEVYR-POST | postúpená vec |
| `Unknown` | nový alebo prázdny stav | text je v `StatusText` |
