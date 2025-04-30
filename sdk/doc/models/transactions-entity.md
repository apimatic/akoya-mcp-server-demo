
# Transactions Entity

Optionally paginated array of transactions

## Structure

`TransactionsEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`Links \| undefined`](../../doc/models/links.md) | Optional | - |
| `transactions` | [`TransactionsEntityTransactions[] \| undefined`](../../doc/models/containers/transactions-entity-transactions.md) | Optional | This is Array of a container for any-of cases. |

## Example (as JSON)

```json
{
  "links": {
    "next": {
      "href": "href4"
    },
    "prev": {
      "href": "href8"
    }
  },
  "transactions": [
    {
      "depositTransaction": {
        "accountId": "accountId0",
        "amount": 1.72,
        "category": "category8",
        "debitCreditMemo": "DEBIT",
        "description": "description0"
      }
    }
  ]
}
```

