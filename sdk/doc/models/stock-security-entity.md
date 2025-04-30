
# Stock Security Entity

Information about the stock security specific to the type of security

## Structure

`StockSecurityEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `unitsStreet` | `number \| undefined` | Optional | Units in the FI's street name, positive quantity |
| `unitsUser` | `number \| undefined` | Optional | Units in user's name directly, positive  quantity |
| `reinvestDividends` | `boolean \| undefined` | Optional | Reinvest dividends |
| `stockType` | [`StockTypeEnum \| undefined`](../../doc/models/stock-type-enum.md) | Optional | - |
| `yield` | `number \| undefined` | Optional | Current yield |
| `yieldAsOfDate` | `string \| undefined` | Optional | Yield as-of date |

## Example (as JSON)

```json
{
  "unitsStreet": 117.56,
  "unitsUser": 92.52,
  "reinvestDividends": false,
  "stockType": "STOCK",
  "yield": 211.18
}
```

