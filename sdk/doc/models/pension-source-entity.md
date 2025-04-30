
# Pension Source Entity

Information about a pension source.

## Structure

`PensionSourceEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `displayName` | `string \| undefined` | Optional | Name of the Source |
| `amount` | `number \| undefined` | Optional | Benefit Amount |
| `paymentOption` | `string \| undefined` | Optional | Form of payment |
| `asOfDate` | `string \| undefined` | Optional | Date benefit was calculated |
| `frequency` | [`FrequencyEnum \| undefined`](../../doc/models/frequency-enum.md) | Optional | - |
| `startDate` | `string \| undefined` | Optional | Assumed retirement date ‐ As of date amount is payable |

## Example (as JSON)

```json
{
  "displayName": "displayName8",
  "amount": 9.06,
  "paymentOption": "paymentOption0",
  "asOfDate": "2016-03-13T12:52:32.123Z",
  "frequency": "ANNUALLY"
}
```

