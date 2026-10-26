#### VehicleFleet
| Parameter | Popis |
| ----------- | ----------- |
| **Year** | rok štatistiky vozového parku (napr. `2026`) |
| **ActiveCount** | počet aktuálne aktívnych vozidiel (na webe „Počet aktuálne aktívnych vozidiel“) |
| **Url** | odkaz na záložku Vozový park |
| **VehicleCount** <i data-tier="ultimate"></i> | počet vozidiel v priebehu roka `Year` (na webe „Počet vozidiel v priebehu roka“). Z tohto počtu sú vypočítané všetky rozpady nižšie |
| **OwnershipTypes** <i data-tier="ultimate"></i> | rozpad podľa typu vlastníctva [`VehicleFleetItem`](#VehicleFleetItem), `Type`: `Owned` (vlastnené), `Leased` (v leasingu) |
| **VehicleTypes** <i data-tier="ultimate"></i> | rozpad podľa typu vozidla [`VehicleFleetItem`](#VehicleFleetItem), od najpočetnejšieho, `Type`: `PassengerCar` (osobné auto), `Truck` (nákladný automobil), `Trailer` (príves/náves), `Tractor` (traktor), `Bus` (autobus), `Motorcycle` (motocykel), `Other` (ostatné vozidlá) |
| **ProductionYears** <i data-tier="ultimate"></i> | rozpad podľa veku vozidla [`VehicleFleetItem`](#VehicleFleetItem), `Type`: `UpTo3` (do 3 rokov), `UpTo8` (do 8 rokov), `UpTo12` (do 12 rokov), `Over12` (viac ako 12 rokov), `Undefined` (nedefinovaný rok výroby) |
| **TopBrands** <i data-tier="ultimate"></i> | 5 najčastejších značiek a položka `Other` (ostatné značky) [`VehicleFleetBrand`](#VehicleFleetBrand) |
