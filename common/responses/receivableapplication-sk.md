#### ReceivableApplication
Jedna prihláška pohľadávok v konaní. Zodpovedá jednému riadku na webe v záložke Prihlášky pohľadávok. Jednotlivé pohľadávky z prihlášky sa nevracajú, iba ich počet a celková suma.

| Parameter | Popis |
| ----------- | ----------- |
| **Creditor** | veriteľ [`IsirParty`](#IsirParty) – môže byť prázdny, ak sa veriteľa z prihlášky nepodarilo priradiť |
| **Representative** | zástupca veriteľa [`IsirParty`](#IsirParty), iba `Name` a `Ico` – môže byť prázdny |
| **PublishDate** | dátum zverejnenia prihlášky vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **ClaimsCount** | počet pohľadávok v prihláške (na webe „Pohľadávky“) – môže byť prázdny |
| **TotalAmount** | celková suma pohľadávok v prihláške v CZK (na webe „Celková suma“) – môže byť prázdny |
