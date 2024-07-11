# API Inteligentný reporting
Táto verzia FinStat API slúži na vyžiadanie vygenerovaných reportov v rámci služby [FinStat Inteligentný reporting](https://www.finstat.sk/inteligentny-reporting)

## Zoznam tém
Výpis všetkých tém [`ReportingTopic`](#ReportingTopic), ktoré služba **Inteligentný reporting** poskytuje.
> **Dopytovaná URL**: ```https://www.finstat.sk/api/getreportingtopics```<br />
> **Hash parameter**: reporting-topics
### Parametre
[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getreportingtopics?apikey=YourAPIKey&hash=af2214dd6e123923b19308a1ef02f5f75a2ed4f0c2ed8e7a477b6612fb18c4f5&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Výpis témy
Výpis všetkých uložených reportov [`ReportOutput`](#ReportOutput) z danej témy reportingu. 
> **Upozornenie:** Reporty staršie ako retenčné obdobie 90 dní sú automaticky vymazávane.

Požiadavka vyžaduje parameter *topic*. Jeho hodnota je získaná pomocou požiadavky [Zoznam tém](#zoznam-tém)
> **Dopytovaná URL**: ```https://www.finstat.sk/api/getreportinglist```<br />
> **Hash parameter**: reporting-list|*{topic}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **topic**<br />*[povinný]*| ID témy reportingu ako je uvedené v zozname tém |

[](../../../common/parameters/parameters-sk.md ':include')

> **Príklad volania:** ```https://www.finstat.sk/api/getreportinglist?topic=topic1&apikey=YourAPIKey&hash=bbcab20d6a0730a5fc4a3bcc87199e4a213dba6d330ed748c00bde4df58be45d&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-sk.md ':include')

## Stiahnutie reportu
Stiahnutie **Excel(.xlsx)** súboru obsahjúceho záznamy vyhovujúce vami definovanému scenáru.
Dopyt vráti dáta požadovaného **.xlsx** súboru

Požiadavka vyžaduje parameter *filename*. Jeho hodnota je získaná pomocou požiadavky [Výpis témy](#výpis-témy)
> **Dopytovaná URL**: ```https://www.finstat.sk/api/getreportingoutput```<br />
> **Hash parameter**: *{filename}*

### Parametre
| Parameter | Popis |
| ----------- | ----------- |
| **filename**<br />*[povinný]*| Identifikátor výstupu z výpisu tém |

[](../../../common/parameters/parameters-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

> **Príklad volania:** ```https://www.finstat.sk/api/getreportingoutput?filename=topic1_file&apikey=YourAPIKey&hash=058683cd75e1486a0dc84fa59ea682c27a99ffd73518979e9a2afebb6694b49c&StationId=YourStationID&StationName=Your+Station+Name```

#### Návratové HTTP error kódy:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-sk.md ':include')

# Štruktúra odpovedí

[](../../../common/responses/reportingtopic-sk.md ':include')

[](../../../common/responses/reportoutput-sk.md ':include')

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovedí
[](../../../common/examples/reporting-topics.md ':include')

[](../../../common/examples/reporting-list.md ':include')