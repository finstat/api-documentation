#### RZPPerson
| Parameter | Popis |
| ----------- | ----------- |
| **FullName** | celé meno vrátane titulov |
| **BirthDate** | dátum narodenia vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Function** | funkcia: `Entrepreneur` (podnikateľ), `ResponsiblePerson` (zodpovedná osoba) |
| **FunctionFrom** | dátum vzniku funkcie vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Subjects** | zoznam predmetov podnikania z RŽP, za ktoré je osoba zodpovedná `string`. Texty sú rovnaké ako v [`Subject`](#Subject). Vypĺňa sa iba pri `ResponsiblePerson`; pri `Entrepreneur` a pri osobe bez predmetov podnikania v XML chýba, v JSON je `null` |
