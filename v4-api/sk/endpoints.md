# Endpointy
## Detail
Tento endpoint poskytuje dáta o spoločnosti identifikovanej pomocou ID
### Parametre

| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **Id** | `string` | ID firmy |
| **ValidateVat** | `boolean` |Ak je zadané „true“, počas volania sa overí VAT subjektu |

#### Hlavička

| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **cp-Apim-Subscription-Key** | `string` | API kľuč |

V tejto ukážke je volanie na slovenskú spoločnosť s ID 47165367
> **Príklad volania:** ```GET https://api.hithorizons.com/invoicing/sk/Company/Detail?id=47165367 HTTP/1.1 Host: api.hithorizons.com Ocp-Apim-Subscription-Key: YOUR_API_KEY```

# Štruktúra odpovede

#### CompanyDetailResult

| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **Id** | `string` | ID firmy |
| **CompanyName** | `string` | oficiálny názov firmy |
| **CompanyAlternativeName** | `string` | alternatívny názov firmy |
| **RegisteredAddress** | [`Address`](v4-api/sk/endpoints.md?id=address) | registrovaná adresa firmy |
| **AdditionalAddresses** | [`AdditionalAddress[]`](v4-api/sk/endpoints.md?id=additionaladdress) | zoznam doplnkových adries firmy |
| **Status** | `string` | stav firmy |
| **IncorporationDate** | `Date` | dátum založenia firmy |
| **DissolutionDate** | `Date` | dátum zrušenia firmy |
| **NationalId** | `string` | ID firmy v národnom formáte |
| **TaxId** | `string` | identifikačné číslo pre DPHH |
| **VatId** | `string` | daňové identifikačné číslo |
| **VatValidationResult** | `string` | v prípade overovania VAT bude vrátená jedna z nasledovných možností: <ul><li>valid - IČ DPH vo VatId bolo overené vexterej službe a momentálne je platné</li><li>invalid - IČ DPH v VatId bolo overené v externej službe a momentálne je neplatné</li><li>error: [textový popis chyby] - počas overovania došlo k chybe</li></ul> Ak sa nepožadovalo overenie, hodnota v tomto poli je `null` |
| **VatValidationDate** | `Date` | Keď sa požadovalo overenie VAT, parameter obsahuje dátum overenia. API vracia v tomto poli iba aktuálny dátum. Ak sa nepožadovalo overenie, hodnota v tomto poli je `null`. |
| **ParentId** | `string` | ID materskej spoločnosti |
| **Idents** | [`CompanyIdent[]`](v4-api/sk/endpoints.md?id=companyident) | Súbor ďalších identifikátorov spoločnosti. Môže obsahovať alternatívne národné identifikátory atď. Toto pole môže byť prázdne alebo prázdne vtedy, ak nie sú k dispozícii žiadne ďalšie identifikátory sú pre spoločnosť |
| **Inactive** | `boolean` | príznak neaktívnej firmy – táto informácia nemusí byť vždy dostupná, a preto hodnota false nemusí vždy znamenať, že je firma aktívna |

#### Address
| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **AddressStreet** | `string` | ulica |
| **StreetNumber** | `string` | číslo ulice |
| **Locality** | `string` | lokalita – zvyčajne administratívny región nízkej úrovne |
| **District** | `string` |okres – zvyčajne administratívny región strednej úrovne |
| **Region** | `string` | raj - zvyčajne administratívny región vysokej úrovne |
| **PostalCode** | `string` | PSČ |
| **City** | `string` | mesto |
| **Country** | `string` | krajina |

#### AdditionalAddress
| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **Type** | `string` | typ adresy |
| **AddressStreet** | `string` | ulica |
| **StreetNumber** | `string` | číslo ulice |
| **Locality** | `string` | lokalita – zvyčajne administratívny región nízkej úrovne |
| **District** | `string` |okres – zvyčajne administratívny región strednej úrovne |
| **Region** | `string` | raj - zvyčajne administratívny región vysokej úrovne |
| **PostalCode** | `string` | PSČ |
| **City** | `string` | mesto |
| **Country** | `string` | krajina |

#### CompanyIdent
| Parameter | Typ | Popis |
| ----------- | ----------- | ----------- |
| **Type** | `string` | typ identifikátora |
| **Value** | `string` | hodnota identifikátora |

> **Poznámka:** poradie nemusí zodpovedať uvedenému zoznamu

# Príklad XML odpovede
``` json
{
    "Success": true,
    "Error": null,
    "Result": {
        "Id": "47165367",
        "CompanyName": "FinStat, s. r. o.",
        "CompanyAlternativeName": null,
        "RegisteredAddress": {
            "AddressStreet": "Ľudmily Kraskovskej",
            "StreetNumber": "1402/14",
            "Locality": null,
            "District": "Bratislava V",
            "Region": "Bratislavský",
            "PostalCode": "85110",
            "City": "Bratislava",
            "Country": "SK"
        },
        "AdditionalAddresses": null,
        "Status": null,
        "IncorporationDate": "2013-05-18",
        "DissolutionDate": null,
        "NationalId": "47165367",
        "TaxId": "2023771332",
        "VatId": "SK2023771332",
        "VatValidationResult": null,
        "VatValidationDate": null,
        "ParentId": null,
        "Idents": null,
        "Inactive": false
    }
}
```

