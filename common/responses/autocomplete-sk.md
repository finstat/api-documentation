#### ApiAutoComplete
| Parameter | Popis |
| ----------- | ----------- |
| **Results** | zoznam [`Company`](#Company) elementov, ktoré vyhovujú zadanému query výrazu (prvých 20 výsledkov)|
| **Suggestions** | zoznam návrhov správneho výrazu pre autocomplete `string` (prvých 10 výrazov) |

#### Company
| Parameter | Popis |
| ----------- | ----------- |
| **Ico** | IČO firmy |
| **Name** | Názov firmy |
| **City** | mesto sídla firmy |
| **Cancelled** | informácia, či bola firma zrušená (`true/false`)|