
# Account Holder Entity

Extends `Customer` and adds a `relationship` field to define the customer's relationship with an account

## Structure

`AccountHolderEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `customer` | [`Customer1 \| undefined`](../../doc/models/customer-1.md) | Optional | Represents a customer (end-user) |
| `relationship` | [`AccountHolderRelationship2Enum \| undefined`](../../doc/models/account-holder-relationship-2-enum.md) | Optional | Customer's relationship to the account |

## Example (as JSON)

```json
{
  "customer": {
    "customerId": "customerId4",
    "name": {
      "first": "first6",
      "middle": "middle6",
      "last": "last0",
      "prefix": "prefix8",
      "suffix": "suffix0"
    },
    "addresses": [
      {
        "type": "HOME",
        "line1": "line16",
        "line2": "line28",
        "line3": "line36",
        "city": "city4"
      }
    ],
    "telephones": [
      {
        "number": "number4",
        "type": "CELL",
        "country": "country0"
      },
      {
        "number": "number4",
        "type": "CELL",
        "country": "country0"
      },
      {
        "number": "number4",
        "type": "CELL",
        "country": "country0"
      }
    ],
    "email": [
      "email8",
      "email9",
      "email0"
    ]
  },
  "relationship": "TRUSTEE"
}
```

