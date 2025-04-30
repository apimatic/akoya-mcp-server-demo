
# Balances

## Structure

`Balances`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accounts` | [`BalancesAccounts[] \| undefined`](../../doc/models/containers/balances-accounts.md) | Optional | This is Array of a container for any-of cases. |

## Example (as JSON)

```json
{
  "accounts": [
    {
      "depositAccount": {
        "accountId": "accountId0",
        "accountType": "accountType0",
        "accountNumberDisplay": "accountNumberDisplay6",
        "currency": {
          "currencyCode": "currencyCode0",
          "currencyRate": 27.48,
          "originalCurrencyCode": "originalCurrencyCode4"
        },
        "description": "description0"
      }
    }
  ]
}
```

