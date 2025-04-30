
# Holding

## Structure

`Holding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `holdingId` | `string \| undefined` | Optional | Long term persistent identity of the holding |
| `securityId` | `string \| undefined` | Optional | Unique identifier of the security. |
| `securityIdType` | [`SecurityIdTypeEnum \| undefined`](../../doc/models/security-id-type-enum.md) | Optional | Security identifier type |
| `taxLots` | [`TaxLot1[] \| undefined`](../../doc/models/tax-lot-1.md) | Optional | Breakdown by tax lot.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |

## Example (as JSON)

```json
{
  "holdingId": "holdingId4",
  "securityId": "securityId6",
  "securityIdType": "CUSIP",
  "taxLots": [
    {
      "costBasis": 131.38,
      "currentValue": 199.34,
      "originalPurchaseDate": "2016-03-13T12:52:32.123Z",
      "positionType": "LONG",
      "purchasedPrice": 176.16
    },
    {
      "costBasis": 131.38,
      "currentValue": 199.34,
      "originalPurchaseDate": "2016-03-13T12:52:32.123Z",
      "positionType": "LONG",
      "purchasedPrice": 176.16
    }
  ]
}
```

