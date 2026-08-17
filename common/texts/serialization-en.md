### Response format and empty values
The API response is in **XML** (default) or **JSON** format (see the *JSON Support* chapter).
The XML response is serialized directly from the response data model — **we do not publish any
WSDL or XSD schema and no such schema is part of the API contract**. This documentation is the
binding description of the response structures.

> **Warning:** No response parameter is guaranteed to be present. If we have no value for a given
item, it is not included in the response — even when its parent element is present.

In the XML response a missing value shows up in two different ways, depending on the data type:

| Data type | Missing value in XML |
| ----------- | ----------- |
| text value (e.g. `Status`, `EnterReason`) | the element is **not included at all** |
| list (e.g. `Officers`, `Persons`) | the element is **not included at all**; an empty list is returned as an empty element, e.g. ```<Deadlines />``` |
| date, number, enumeration (e.g. `ExitDate`, `EmployeesNumber`, `Source`) | the element **is present** with the ```xsi:nil="true"``` attribute, e.g. ```<ExitDate xsi:nil="true" />``` |

``` xml
<Bankrupt>
  <EnterDate>2011-05-19T00:00:00</EnterDate>
  <ExitDate xsi:nil="true" />
  <Source>CommercialBulletin</Source>
  <Deadlines />
  <StartDate xsi:nil="true" />
</Bankrupt>
```

In the example above the text elements `Status`, `EnterReason`, `ExitReason`, `FileReference` and
`CourtCode` are not included, because we have no such values for that proceeding. The `Officers`
list is not included either.

In the JSON response all parameters are present, missing values are returned as ```null```.

> **Integration note:** If you generate an XSD schema from a sample response on your side, the
resulting schema will incorrectly mark every element that happened to have a value in the sample
as mandatory. Set ```minOccurs="0"``` for text elements and lists, and ```nillable="true"``` for
date, number and enumeration elements.
