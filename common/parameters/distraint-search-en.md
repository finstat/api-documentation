| Parameter | Description |
| ----------- | ----------- |
| **search**<br />*[mandatory]* | format `{ico}\|{surname}\|{dateOfBirth}\|{city}\|{companyName}\|{fileReference}`. Unused partameters can be empty or set to `null`.|

- **ico** -	company identification nummber
- **surname** -	surname
- **dateOfBirth** -	date of birth in the `dd.MM.yyyy` format
- **city** - city/town
- **companyName** -	company name
- **fileReference** - court reference file number

##### Validations of the `search` parameter
Violating any of them returns **HTTP 400** with the reason in the response body:

| Validation | Response body |
| ----------- | ----------- |
| the parameter must contain **exactly 6 parts** separated by `\|` (i.e. 5 separators), even when some of the parts are empty | ```not all search parameters are specified!``` |
| **at least one** of `ico`, `companyName`, `fileReference`, `surname` must be filled in | ```search parameters not specified!``` |
| when `ico` is filled in, it must be a valid company identification number | ```Invalid 'ico' parameter!``` |
| when `surname` is filled in, `dateOfBirth` **or** `city` must be filled in as well | ```parameter 'surname' requires parameter 'dateOfBirth' or 'city'!``` |
| when `dateOfBirth` is filled in, it must use the `dd.MM.yyyy` format | ```Invalid 'dateOfBirth' parameter, expected format 'dd.MM.yyyy'!``` |

> **Note:** the individual parts are trimmed of surrounding whitespace before they are evaluated.
