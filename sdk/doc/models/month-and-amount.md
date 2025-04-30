
# Month and Amount

Month and amount pair used on IRS Form 1099-K, etc.

## Structure

`MonthAndAmount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `month` | [`MonthAbbreviation1Enum \| undefined`](../../doc/models/month-abbreviation-1-enum.md) | Optional | Month |
| `amount` | `number \| undefined` | Optional | Amount |

## Example (as JSON)

```json
{
  "month": "SEP",
  "amount": 97.94
}
```

