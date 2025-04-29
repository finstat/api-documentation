#### ReceivableDebt
| Parameter | Popis |
| ----------- | ----------- |
| **Source** | Správca |
| **Value** | hodnota pohľadávky |
| **ValidFrom** | dátum detekovania dlhu vo formáte `RRRR-MM-DDTHH:MM:SS` |

#### Office
| Parameter | Popis |
| ----------- | ----------- |
| **Street** | ulica |
| **StreetNumber** | popisné čislo budovy |
| **City** | mesto |
| **ZipCode** | PSČ |
| **District** | okres |
| **Region** | kraj |
| **Country** | krajina/štát |
| **Subjects** | zoznam predmetov podnikania `string` |
| **Type** | typ adresy |

#### JudgementCount
| Parameter | Popis |
| ----------- | ----------- |
| **Name** | typ zastúpenia v súdnom rozhodnutí <ul><li>Defendant – odporca</li><li>Plaintiff – navrhovateľ</li><li>Attorney - zástupca</li></ul> |
| **Value** | počet rozhodnutí za dané zastúpenie |

#### Person
| Parameter | Popis |
| ----------- | ----------- |
| **FullName** | celé meno - v prípade že je to firma, tak obsahuje názov firmy |
| **Street** | ulica osoby |
| **StreetNumber** | popisné čislo budovy |
| **City** | mesto |
| **District** | okres |
| **Region** | kraj |
| **Country** | štát |
| **DepositAmount** | výška vkladu |
| **PaybackRange** | rozsah splatenia |
| **DetectedFrom** | dátum, od ktorého je vo finstat.sk táto osoba na danej pozícii detekovaná (obsahuje dátum poslednej zmeny) vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | dátum, do ktorého je detekovaná v prípade historických dát vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Functions** | zoznam funkcií osoby vo firme [`FunctionAssigment`](#FunctionAssigment) |
| **StructuredName** | obsahuje rozdelený obchodný názov na jednotlivé časti [`StructuredName`](#StructuredName) |
| **ICO** | IČO osoby v prípade firmy - môže byť prázdne |

#### RpvsPerson
| Parameter | Popis |
| ----------- | ----------- |
| **FullName** | celé meno - v prípade že je to firma, tak obsahuje názov firmy |
| **Street** | ulica osoby |
| **StreetNumber** | popisné čislo budovy |
| **City** | mesto |
| **District** | okres |
| **Region** | kraj |
| **Country** | štát |
| **ICO** | IČO osoby v prípade firmy - môže byť prázdne |
| **BirthDate** | dátum narodenia |
| **DetectedFrom** | dátum, od ktorého je vo finstat.sk táto osoba na danej pozícii detekovaná (obsahuje dátum poslednej zmeny) vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **DetectedTo** | dátum, do ktorého je detekovaná v prípade historických dát vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |
| **Functions** | zoznam funkcií osoby vo firme [`FunctionAssigment`](#FunctionAssigment) |
| **StructuredName** | obsahuje rozdelený obchodný názov na jednotlivé časti [`StructuredName`](#StructuredName) 

#### StructuredName
| Parameter | Popis |
| ----------- | ----------- |
| **Prefix** | zoznam titulov pred menom `string` |
| **Name** | meno (max 2 položky) `string`|
| **Suffix** | zoznam titulov za menom `string` |
| **Name** | všetky ostatné slová za menom `string` |

#### Court
| Parameter | Description |
| ----------- | ----------- |
| **Name** | názov ak je dostupný |
| **Street** | ulica ak je dostupná |
| **StreetNumber** | popisné číslo ak je dostupné |
| **ZipCode** | PSČ ak je dostupné |
| **City** | Mesto ak je dostupné |
| **District** | okres ak je dostupný |
| **Region** | kraj ak je dostupný |
| **Country** | krajina ak je dostupná |

#### HistoryAddress
| Parameter | Popis |
| ----------- | ----------- |
| **Street** | ulica osoby |
| **StreetNumber** | popisné čislo budovy |
| **City** | mesto |
| **ZipCode** | PSČ |
| **District** | okres |
| **Region** | kraj |
| **Country** | štát |
| **ValidFrom** | dátum, od ktorého je detekovaná platná vo formáte `RRRR-MM-DDTHH:MM:SS` |
| **ValidTo** | dátum, do ktorého je detekovaná vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |

#### ProceedingResult
| Parameter | Popis |
| ----------- | ----------- |
| **FileReference** | spisová značka |
| **CourtCode** | kód súdu |
| **StartDate** | dátum začatia podľa registra úpadcov|
| **EnterDate** | dátum vyhlásenie |
| **EnterReason** | dôvod začatia procesu podľa ORSR |
| **ExitDate** | dátum ukončenia konania |
| **ExitReason** | dôvod ukončenia konania |
| **Source** | zdroj <ul><li>BankruptcyRegister (Register úpadcov)</li><li>CommercialBulletin (Obchodný vestník)</li><li>CompaniesRegister (Obchodný register)</li></ul> |
| **Officer** | správca [`Person`](#Person) |
| **Deadlines** | zoznam aktuálnych lehôt [`Deadline`](#Deadline) |
| **Status** | stav konania podľa Registra úpadcov |
| **ProposalDate** |  dátum návrhu vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny|
| **CourtPublishingDate** |  dátum zverejnenia na súde vo formáte `RRRR-MM-DDTHH:MM:SS` – môže byť prázdny |

#### BankruptResult
Štruktúra parametrov je totožná s [`ProceedingResult`](#ProceedingResult)

#### RestructuringResult
Štruktúra parametrov je totožná s [`ProceedingResult`](#ProceedingResult)

#### LiquidationResult
| Parameter | Popis |
| ----------- | ----------- |
| **EnterDate** | dátum vstupu |
| **EnterReason** | dôvod vstupu |
| **ExitDate** | dátum výstupu |
| **Source** | zdroj <ul><li>CompaniesRegister (Obchodný register)</li></ul> |
| **Officer** | správca [`Person`](#Person) |
| **Deadline** | popis lehoty |
| **LiquidatorProcedure** | konanie |
| **CancelReason** |  dôvod rušenia |
| **DeleteReason** |  dôvod vymazania|

#### Deadline
| Parameter | Popis |
| ----------- | ----------- |
| **Type** | popis lehoty (napr. Lehota na Popieranie pohľadávok) |
| **Date** | Dátum lehoty vo formáte `RRRR-MM-DDTHH:MM:SS` |

#### IncorporationDate
| Parameter | Popis |
| ----------- | ----------- |
| **Date** | dátum vvzniku vo formáte `RRRR-MM-DDTHH:MM:SS`|
| **Source** | zdroj |

#### DissolutionDate
| Parameter | Popis |
| ----------- | ----------- |
| **Date** | dátum zániku vo formáte `RRRR-MM-DDTHH:MM:SS`|
| **Source** | zdroj |