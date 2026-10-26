##### EliteCZ parametre:
| Parameter | Popis |
| ----------- | ----------- |
| **VatGroupMember** | príznak, či je aktuálna registrácia k DPH registráciou skupiny DPH (`true/false`) |
| **FinancialIndicators** | finančné ukazovatele za posledné <span data-tier="elite">2 roky</span><span data-tier="ultimate">4 roky</span> [`FinancialIndicators`](#FinancialIndicators). Ak subjekt nemá finančné údaje: v XML chýba, v JSON je `null` |
| **OtherCzNaces** | zoznam vedľajších aktívnych CZ NACE [`CzNace`](#CzNace). Ak je prázdny, v odpovedi chýba |
| **Contacts** | zoznam kontaktov [`Contact`](#Contact). Ak subjekt nemá žiadny kontakt: v XML chýba, v JSON je `null` |
| **Offices** | prevádzky z Registra živnostenského podnikania [`Offices`](#Offices). Vracia sa vždy; pri subjektoch, ktoré nie sú v RŽP alebo nemajú aktívnu prevádzku, je `Count` 0 |
| **VehicleFleet** | vozový park [`VehicleFleet`](#VehicleFleet). Ak subjekt nemá štatistiku vozidiel: v XML chýba, v JSON je `null` |
| **IsirProceedings** | zoznam aktívnych insolvenčných konaní, v ktorých je subjekt dlžníkom [`IsirProceeding`](#IsirProceeding). Ukončené konania sa nevracajú. Ak je prázdny, v odpovedi chýba |
