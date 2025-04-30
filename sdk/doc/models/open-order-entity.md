
# Open Order Entity

Information on an open order.

## Structure

`OpenOrderEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `orderId` | `string \| undefined` | Optional | Long term persistent identity of the order. Id for this order transaction. |
| `securityId` | `string \| undefined` | Optional | Unique identifier of the security. |
| `securityIdType` | [`SecurityIdTypeEnum \| undefined`](../../doc/models/security-id-type-enum.md) | Optional | Security identifier type |
| `symbol` | `string \| undefined` | Optional | Market symbol |
| `description` | `string \| undefined` | Optional | Description of order |
| `units` | `number \| undefined` | Optional | Number of units (shares, bonds, etc.) |
| `orderType` | [`OrderTypeEnum \| undefined`](../../doc/models/order-type-enum.md) | Optional | Type of order. |
| `orderDate` | `string \| undefined` | Optional | Order date |
| `unitPrice` | `number \| undefined` | Optional | Unit price |
| `unitType` | [`UnitTypeEnum \| undefined`](../../doc/models/unit-type-enum.md) | Optional | Type of unit. |
| `orderDuration` | [`OrderDurationEnum \| undefined`](../../doc/models/order-duration-enum.md) | Optional | This order is good for DAY, GOODTILLCANCEL, IMMEDIATE |
| `subAccount` | [`SubAccountEnum \| undefined`](../../doc/models/sub-account-enum.md) | Optional | - |
| `limitPrice` | `number \| undefined` | Optional | Limit Price |
| `stopPrice` | `number \| undefined` | Optional | Stop price |
| `inv401kSource` | [`Inv401kSourceEnum \| undefined`](../../doc/models/inv-401-k-source-enum.md) | Optional | For 401(k) accounts, source of money for this order. Default if not present is OTHERNONVEST. |

## Example (as JSON)

```json
{
  "orderId": "orderId4",
  "securityId": "securityId6",
  "securityIdType": "VALOR",
  "symbol": "symbol0",
  "description": "description2"
}
```

