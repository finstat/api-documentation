#### Function
| Parameter | Popis |
| ----------- | ----------- |
| **Type** | kód funkcie (zoznam nižšie) |
| **TypeText** | popis funkcie v jazyku odpovede |
| **Description** | názov funkcie tak, ako je zapísaný v registri (napr. `jednatel`, `člen představenstva`) |
| **From** | dátum vzniku funkcie vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |

Kódy funkcií (`Type`):

* **Základné:** `Statutory` (štatutár), `Partner` (spoločník), `Shareholder` (akcionár), `SupervisoryBoard` (dozorná rada), `ControlCommission` (kontrolná komisia), `Procuration` (prokúra), `Liquidator` (likvidátor), `BankruptcyAdministrator` (insolvenčný správca), `RestructuringAdministrator` (správca reštrukturalizácie), `LegalSuccessor` (právny nástupca), `Merger` (zlúčenie), `Division` (rozdelenie), `ForeignPerson` (zahraničná osoba), `ForeignPersonStatutory` (štatutár zahraničnej osoby).
* **Skutoční majitelia:** `BeneficialOwner` a upresnenia `BeneficialOwnerTopManagement`, `BeneficialOwnerAppointmentRight`, `BeneficialOwnerFundsRecipient`, `BeneficialOwnerManagingBody`, `BeneficialOwnerFounder`, `BeneficialOwnerBenefitRight`, `BeneficialOwnerVotingRight`, `BeneficialOwnerShareCapital`, `BeneficialOwnerSignificantBenefit`, `BeneficialOwnerJointAction`, `BeneficialOwnerOtherControl`, `BeneficialOwnerUnspecified`, `BeneficialOwnerDirect`, `BeneficialOwnerIndirect`, `BeneficialOwnerSubstitute`, `BeneficialOwnerSection4`, `BeneficialOwnerSection6`, `BeneficialOwnerRestricted`.
* **Register partnerov verejného sektora:** `AuthorizedPerson`, `PublicSectorPartnerBeneficialOwner`, `PublicOfficial`.
* **Živnostenský register:** `ResponsiblePerson` (zodpovedná osoba), `Entrepreneur` (podnikateľ).
* **Ostatné:** `Other`.

Zoznam kódov je spoločný pre CZ aj SK API. V odpovedi sa vracajú iba kódy, ktoré daný register obsahuje.
