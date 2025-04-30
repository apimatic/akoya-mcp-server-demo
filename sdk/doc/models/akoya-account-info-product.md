
# Akoya Account Info Product

## Structure

`AkoyaAccountInfoProduct`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accounts` | [`AkoyaAccountInfoProductAccounts[] \| undefined`](../../doc/models/containers/akoya-account-info-product-accounts.md) | Optional | This is Array of a container for any-of cases. |

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
    },
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

