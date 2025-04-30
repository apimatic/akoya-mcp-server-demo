
# Holding 1

## Structure

`Holding1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `holdingId` | `string \| undefined` | Optional | - |
| `securityId` | `string \| undefined` | Optional | - |
| `securityIdType` | `string \| undefined` | Optional | - |
| `taxLots` | [`TaxLot2[] \| undefined`](../../doc/models/tax-lot-2.md) | Optional | - |

## Example (as JSON)

```json
{
  "holdingId": "holdingId4",
  "securityId": "securityId6",
  "securityIdType": "securityIdType2",
  "taxLots": [
    {
      "originalPurchaseDate": "originalPurchaseDate8",
      "quantity": 32,
      "purchasedPrice": 208,
      "costBasis": 131.38,
      "currentValue": 222
    },
    {
      "originalPurchaseDate": "originalPurchaseDate8",
      "quantity": 32,
      "purchasedPrice": 208,
      "costBasis": 131.38,
      "currentValue": 222
    },
    {
      "originalPurchaseDate": "originalPurchaseDate8",
      "quantity": 32,
      "purchasedPrice": 208,
      "costBasis": 131.38,
      "currentValue": 222
    }
  ]
}
```

