#### FiledInsolvencyClaims
Prihlášky pohľadávok, ktoré subjekt podal ako veriteľ, iba v aktívnych insolvenčných konaniach.

| Parameter | Popis |
| ----------- | ----------- |
| **ProceedingsCount** | počet všetkých aktívnych insolvenčných konaní, v ktorých subjekt vystupuje ako veriteľ |
| **AmountOfClaims** | celková suma pohľadávok prihlásených subjektom vo všetkých aktívnych konaniach v CZK, bez odmietnutých prihlášok – môže byť prázdny |
| **Applications** | prihlášky z najviac 300 naposledy aktívnych konaní, od najnovšej, najviac 300 položiek [`FiledClaimApplication`](#FiledClaimApplication) |

`ProceedingsCount` a `AmountOfClaims` zahŕňajú všetky aktívne konania, zoznam `Applications` je obmedzený. Pri veľkých veriteľoch (banky, úrady) preto zoznam neobsahuje všetky prihlášky.

#### FiledClaimApplication
| Parameter | Popis |
| ----------- | ----------- |
| **FileReference** | spisová značka konania |
| **Url** | odkaz na detail konania |
| **Debtors** | zoznam dlžníkov v konaní [`IsirParty`](#IsirParty) |
| **Representative** | zástupca veriteľa [`IsirParty`](#IsirParty), iba `Name` a `Ico` – môže byť prázdny |
| **PublishDate** | dátum zverejnenia prihlášky vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **ClaimsCount** | počet pohľadávok v prihláške – môže byť prázdny |
| **TotalAmount** | celková suma pohľadávok v prihláške v CZK – môže byť prázdny |
