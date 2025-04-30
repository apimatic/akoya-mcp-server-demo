
# Current Customer

Currently authenticated end-user

## Structure

`CurrentCustomer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `customer` | [`Customer2 \| undefined`](../../doc/models/customer-2.md) | Optional | current customer |

## Example (as JSON)

```json
{
  "customer": {
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
    }
  }
}
```

