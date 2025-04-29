#### IcDphAdditionalData
| Parameter | Popis |
| ----------- | ----------- |
| **IcDph** | číslo IČ DPH aj v prípade, ak firma je v zozname vymazaných subjektov |
| **Paragraph** | paragraf, pre ktorý je číslo DPH vydané aj v prípade, že firma je v zozname vymazaných subjektov |
| **CancelListDetectedDate** | dátum detekovania firmy v zozname subjektov s dôvodom na zrušenie DPH vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **RemoveListDetectedDate** | dátum detekovania firmy v zozname subjektov Zoznam vymazaných platiteľov DPH podľa §52 ods.8 zákona 563/2009 Z. z. `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |

#### CreditScoreState
- **Red** – vysoká pravdepodobnosť úpadku
- **Yellow** – pásmo šedej zóny
- **Green** – finančne stabilná spoločnosť

#### PaymentOrder
| Parameter | Popis |
| ----------- | ----------- |
| **PublishDate** | dátum zverejnenia vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **Value** | hodnota platobného rozkazu  - može byť prázdna |