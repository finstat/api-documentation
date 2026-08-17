### Formát odpovede a prázdne hodnoty
Odpoveď API je vo formáte **XML** (predvolene) alebo **JSON** (viď kapitolu *Podpora JSON*).
XML odpoveď sa serializuje priamo z dátového modelu odpovede — **nepublikujeme žiadnu WSDL ani
XSD schému a takáto schéma nie je súčasťou kontraktu API**. Záväzným opisom štruktúry odpovedí
je táto dokumentácia.

> **Upozornenie:** Žiadny parameter odpovede nie je garantovane prítomný. Ak pre daný údaj
nemáme hodnotu, v odpovedi nebude uvedený — a to aj v prípade, že jeho nadradený element
prítomný je.

V XML odpovedi sa chýbajúca hodnota prejaví dvoma spôsobmi, podľa typu údaja:

| Typ údaja | Chýbajúca hodnota v XML |
| ----------- | ----------- |
| textový údaj (napr. `Status`, `EnterReason`) | element **sa neuvedie vôbec** |
| zoznam (napr. `Officers`, `Persons`) | element **sa neuvedie vôbec**; prázdny zoznam sa uvedie ako prázdny element, napr. ```<Deadlines />``` |
| dátum, číslo, enumerácia (napr. `ExitDate`, `EmployeesNumber`, `Source`) | element **je prítomný** s atribútom ```xsi:nil="true"```, napr. ```<ExitDate xsi:nil="true" />``` |

``` xml
<Bankrupt>
  <EnterDate>2011-05-19T00:00:00</EnterDate>
  <ExitDate xsi:nil="true" />
  <Source>CommercialBulletin</Source>
  <Deadlines />
  <StartDate xsi:nil="true" />
</Bankrupt>
```

V uvedenom príklade nie sú uvedené textové elementy `Status`, `EnterReason`, `ExitReason`,
`FileReference` ani `CourtCode`, pretože pre dané konanie tieto hodnoty nemáme. Rovnako nie je
uvedený zoznam `Officers`.

V JSON odpovedi sú všetky parametre prítomné, chýbajúce hodnoty majú hodnotu ```null```.

> **Poznámka pre integráciu:** Ak si na svojej strane generujete XSD schému z ukážkovej odpovede,
takto vzniknutá schéma bude nesprávne označovať za povinné všetky elementy, ktoré vo vzorke
hodnotu mali. Textovým elementom a zoznamom preto nastavte ```minOccurs="0"``` a dátumovým,
číselným a enumeračným elementom ```nillable="true"```.
