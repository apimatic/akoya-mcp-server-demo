
# Tax Lot 1

## Structure

`TaxLot1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `costBasis` | `number \| undefined` | Optional | Total amount of money spent acquiring this lot including any fees or commission expenses incurred. |
| `currentValue` | `number \| undefined` | Optional | Lot market value |
| `originalPurchaseDate` | `string \| undefined` | Optional | Lot acquired date. |
| `positionType` | [`PositionType2Enum \| undefined`](../../doc/models/position-type-2-enum.md) | Optional | LONG, SHORT. |
| `purchasedPrice` | `number \| undefined` | Optional | Original purchase price. |
| `quantity` | `number \| undefined` | Optional | Lot quantity. |

## Example (as JSON)

```json
{
  "costBasis": 73.74,
  "currentValue": 141.7,
  "originalPurchaseDate": "2016-03-13T12:52:32.123Z",
  "positionType": "LONG",
  "purchasedPrice": 118.52
}
```

