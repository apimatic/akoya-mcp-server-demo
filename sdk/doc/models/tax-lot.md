
# Tax Lot

## Structure

`TaxLot`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `costBasis` | `number \| undefined` | Optional | Total amount of money spent acquiring this lot including any fees or commission expenses incurred. |
| `currentValue` | `number \| undefined` | Optional | Lot market value |
| `originalPurchaseDate` | `string \| undefined` | Optional | Lot acquired date. |
| `postionType` | [`PostionTypeEnum \| undefined`](../../doc/models/postion-type-enum.md) | Optional | LONG, SHORT. |
| `purchasedPrice` | `number \| undefined` | Optional | Original purchase price. |
| `quantity` | `number \| undefined` | Optional | Lot quantity. |

## Example (as JSON)

```json
{
  "costBasis": 225.68,
  "currentValue": 37.64,
  "originalPurchaseDate": "2016-03-13T12:52:32.123Z",
  "postionType": "LONG",
  "purchasedPrice": 14.46
}
```

