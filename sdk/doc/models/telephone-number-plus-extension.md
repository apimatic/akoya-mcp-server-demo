
# Telephone Number Plus Extension

A telephone number that can contain optional text for an arbitrary length telephone extension number

## Structure

`TelephoneNumberPlusExtension`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`TelephoneNumberType2Enum \| undefined`](../../doc/models/telephone-number-type-2-enum.md) | Optional | Type of phone number: HOME, BUSINESS, CELL, FAX |
| `country` | `string \| undefined` | Optional | Country calling codes defined by ITU-T recommendations E.123 and E.164<br><br>**Constraints**: *Maximum Length*: `3` |
| `number` | `string \| undefined` | Optional | Telephone subscriber number defined by ITU-T recommendation E.164<br><br>**Constraints**: *Maximum Length*: `15`, *Pattern*: `\d+` |
| `extension` | `string \| undefined` | Optional | An arbitrary length telephone number extension |

## Example (as JSON)

```json
{
  "type": "FAX",
  "country": "country2",
  "number": "number6",
  "extension": "extension4"
}
```

