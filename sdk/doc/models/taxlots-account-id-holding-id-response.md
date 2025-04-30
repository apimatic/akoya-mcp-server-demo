
# Taxlots Account Id Holding Id Response

## Structure

`TaxlotsAccountIdHoldingIdResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string \| undefined` | Optional | - |
| `holding` | [`Holding1 \| undefined`](../../doc/models/holding-1.md) | Optional | - |

## Example (as JSON)

```json
{
  "accountId": "accountId0",
  "holding": {
    "holdingId": "holdingId0",
    "securityId": "securityId2",
    "securityIdType": "securityIdType6",
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
}
```

