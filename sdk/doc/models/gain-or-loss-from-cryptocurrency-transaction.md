
# Gain or Loss From Cryptocurrency Transaction

Tax information for a single cryptocurrency transaction. If reported on Form 1099-B, use Tax1099B and SecurityDetail instead of this entity.

## Structure

`GainOrLossFromCryptocurrencyTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cryptocurrencyName` | `string \| undefined` | Optional | Cryptocurrency name (e.g. Bitcoin) |
| `symbol` | `string \| undefined` | Optional | Cryptocurrency abbreviation or symbol (e.g. BTC) |
| `quantity` | `number \| undefined` | Optional | Quantity (e.g. 0.0125662) |
| `saleDescription` | `string \| undefined` | Optional | Description of property (1099-B box 1a) |
| `dateAcquired` | `string \| undefined` | Optional | Date acquired (1099-B box 1b) |
| `variousDatesAcquired` | `boolean \| undefined` | Optional | Acquired on various dates (1099-B box 1b) |
| `dateOfSale` | `string \| undefined` | Optional | Date sold or disposed (1099-B box 1c) |
| `salesPrice` | `number \| undefined` | Optional | Proceeds (not price per share, 1099-B box 1d) |
| `costBasis` | `number \| undefined` | Optional | Cost or other basis (1099-B box 1e) |
| `longOrShort` | [`SaleTermType3Enum \| undefined`](../../doc/models/sale-term-type-3-enum.md) | Optional | LONG or SHORT (1099-B box 2) |

## Example (as JSON)

```json
{
  "dateAcquired": "2021-07-15",
  "dateOfSale": "2021-07-15",
  "cryptocurrencyName": "cryptocurrencyName6",
  "symbol": "symbol0",
  "quantity": 100.14,
  "saleDescription": "saleDescription2"
}
```

