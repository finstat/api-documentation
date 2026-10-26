#### FinancialIndicators
Zoznam ukazovateľov [`Indicator`](#Indicator); `Name` nadobúda tieto hodnoty:

| Name | Popis |
| ----------- | ----------- |
| **Profit** | Zisk – výsledok hospodárenia za účtovné obdobie po zdanení |
| **Sales** | Tržby – súčet tržieb z predaja vlastných výrobkov a služieb a tržieb za predaj tovaru |
| **Assets** | Aktíva – celková hodnota majetku spoločnosti |
| **Equity** | Vlastný kapitál – vlastné zdroje financovania spoločnosti, teda kapitál vložený vlastníkmi a zisk, ktorý v spoločnosti zostal |
| **FinancialLeverage** | Finančná páka – aktíva / vlastný kapitál |
| **ShareCapital** | Základné imanie podľa účtovnej závierky |
| **EBIT** | Zisk pred zaplatením daní a úrokov |
| **EBITDA** | Zisk pred zaplatením daní a úrokov a pred započítaním znehodnotenia a amortizácie |
| **ValueAdded** | Pridaná hodnota |
| **ROA** | Návratnosť aktív |
| **ROE** | Návratnosť vlastného kapitálu |
| **LiabilitiesToAssets** | Celková zadlženosť |
| **Depreciation** | Úpravy hodnôt v prevádzkovej oblasti |
| **NetTurnover** | Čistý obrat za účtovné obdobie podľa výkazu ziskov a strát |
| **ROAEbit** | Návratnosť aktív (EBIT) – podiel EBIT k aktívam |

#### Indicator
| Parameter | Popis |
| ----------- | ----------- |
| **Name** | názov ukazovateľa (pozri [`FinancialIndicators`](#FinancialIndicators)) |
| **Values** | hodnoty za jednotlivé roky, od najnovšieho [`IndicatorValue`](#IndicatorValue) |

#### IndicatorValue
| Parameter | Popis |
| ----------- | ----------- |
| **Year** | rok |
| **Value** | hodnota – môže byť prázdna. Sumy sú v CZK, pomerové ukazovatele ako podiel (`0.15` = 15 %) |
