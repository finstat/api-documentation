#### CreditScore
| Parameter | Popis |
| ----------- | ----------- |
| **Name** | kreditný model: `FinStatScore` (FinStat skóre), `AltmanZ` (Altmanovo Z-skóre), `Index05` (Index IN05) |
| **Values** | hodnoty za jednotlivé roky, od najnovšieho [`CreditScoreValue`](#CreditScoreValue) |

#### CreditScoreValue
| Parameter | Popis |
| ----------- | ----------- |
| **Year** | rok |
| **Value** | hodnota modelu, pri `FinStatScore` v percentách – môže byť prázdna |
| **State** | slovné hodnotenie [`CreditScoreState`](#CreditScoreState) – môže byť prázdne |
