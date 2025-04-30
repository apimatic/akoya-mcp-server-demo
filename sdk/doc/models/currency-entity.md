
# Currency Entity

Indicates the currency code used by the account. May also include currency rate.

## Structure

`CurrencyEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currencyCode` | `string \| undefined` | Optional | Iso 4217 currency code. |
| `currencyRate` | `number \| undefined` | Optional | Currency rate between original and converted currency. |
| `originalCurrencyCode` | `string \| undefined` | Optional | Iso 4217 currency code. |

## Example (as JSON)

```json
{
  "currencyCode": "currencyCode4",
  "currencyRate": 203.06,
  "originalCurrencyCode": "originalCurrencyCode0"
}
```

