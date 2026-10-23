#### VehicleFleet
| Parameter | Popis |
| ----------- | ----------- |
| **Year** | rok štatistiky vozového parku (napr. `2026`) |
| **ActiveCount** | počet aktuálne aktívnych vozidiel (na webe „Počet aktuálne aktívnych vozidiel“) |
| **Url** | odkaz na záložku Vozový park |
| **VehicleCount** | iba UltimateCZ: počet vozidiel v priebehu roka `Year` (na webe „Počet vozidiel v priebehu roka“). Z tohto počtu sú vypočítané všetky rozpady nižšie |
| **OwnershipTypes** | iba UltimateCZ: rozpad podľa typu vlastníctva [`VehicleFleetItem`](#VehicleFleetItem), `Type`: `Owned` (vlastnené), `Leased` (v leasingu) |
| **VehicleTypes** | iba UltimateCZ: rozpad podľa typu vozidla [`VehicleFleetItem`](#VehicleFleetItem), od najpočetnejšieho, `Type`: `PassengerCar` (osobné auto), `Truck` (nákladný automobil), `Trailer` (príves/náves), `Tractor` (traktor), `Bus` (autobus), `Motorcycle` (motocykel), `Other` (ostatné vozidlá) |
| **ProductionYears** | iba UltimateCZ: rozpad podľa veku vozidla [`VehicleFleetItem`](#VehicleFleetItem), `Type`: `UpTo3` (do 3 rokov), `UpTo8` (do 8 rokov), `UpTo12` (do 12 rokov), `Over12` (viac ako 12 rokov), `Undefined` (nedefinovaný rok výroby) |
| **TopBrands** | iba UltimateCZ: 5 najčastejších značiek a položka `Other` (ostatné značky) [`VehicleFleetBrand`](#VehicleFleetBrand) |

Položky rozpadov s počtom 0 sa nevracajú.

#### VehicleFleetItem
| Parameter | Popis |
| ----------- | ----------- |
| **Type** | typ položky podľa rozpadu (pozri `VehicleFleet`) |
| **Count** | počet vozidiel |

#### VehicleFleetBrand
| Parameter | Popis |
| ----------- | ----------- |
| **Name** | značka (napr. `ŠKODA`) alebo `Other` |
| **Count** | počet vozidiel |
