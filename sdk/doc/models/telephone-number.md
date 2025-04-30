
# Telephone Number

Standard for international phone numbers

## Structure

`TelephoneNumber`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`TelephoneNumberType2Enum \| undefined`](../../doc/models/telephone-number-type-2-enum.md) | Optional | Type of phone number: HOME, BUSINESS, CELL, FAX |
| `country` | `string \| undefined` | Optional | Country calling codes defined by ITU-T recommendations E.123 and E.164<br><br>**Constraints**: *Maximum Length*: `3` |
| `number` | `string \| undefined` | Optional | Telephone subscriber number defined by ITU-T recommendation E.164<br><br>**Constraints**: *Maximum Length*: `15`, *Pattern*: `\d+` |

## Example (as JSON)

```json
{
  "type": "FAX",
  "country": "country8",
  "number": "number8"
}
```

