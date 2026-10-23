##### UltimateCZ parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **ORCRPersons** | zoznam aktívnych osôb z Obchodního rejstříku (ORČR) [`ORCRPerson`](#ORCRPerson). Ak je prázdny, v odpovedi chýba |
| **RZPPersons** | zoznam aktívnych osôb z Registra živnostenského podnikania (RŽP) [`RZPPerson`](#RZPPerson). Ak je prázdny, v odpovedi chýba |
| **StatutoryAction** | spôsob konania štatutárov, text z ORČR – môže byť prázdny (v XML chýba, v JSON `null`) |
| **ProcurationAction** | spôsob konania prokúry, text z ORČR – môže byť prázdny (v XML chýba, v JSON `null`) |
| **Subjects** | zoznam aktívnych predmetov podnikania [`Subject`](#Subject): pri firmách z ORČR, pri živnostníkoch živnostenské oprávnenia z RŽP. Ak je prázdny, v odpovedi chýba |
| **CreditScores** | kreditné modely za posledné 4 roky [`CreditScore`](#CreditScore). Ak subjekt nemá finančné údaje: v XML chýba, v JSON je `null` |
| **FiledInsolvencyClaims** | prihlášky pohľadávok, ktoré subjekt podal ako veriteľ v aktívnych insolvenčných konaniach [`FiledInsolvencyClaims`](#FiledInsolvencyClaims). Chýba, ak subjekt nie je veriteľom v žiadnom aktívnom konaní |

UltimateCZ navyše rozširuje parametre EliteCZ:

* `Contacts` obsahuje aj webové stránky a sociálne siete (`Web`, `LinkedIn`, `Facebook`, `Instagram`, `X`, `YouTube`, `TikTok`),
* `Offices` obsahuje aj zoznam prevádzok `Items`,
* `VehicleFleet` obsahuje aj rozpady za rok `Year` (`VehicleCount`, `OwnershipTypes`, `VehicleTypes`, `ProductionYears`, `TopBrands`),
* `IsirProceedings` obsahuje rozšírené údaje o konaní (spôsob riešenia, správcovia, veritelia, prihlášky pohľadávok),
* `FinancialIndicators` sú za posledné 4 roky.
