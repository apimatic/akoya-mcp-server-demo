
# Account Contact Entity

Contact information for the account

## Structure

`AccountContactEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `holders` | [`AccountHolderEntity[] \| undefined`](../../doc/models/account-holder-entity.md) | Optional | Owners of the account |
| `emails` | `string[] \| undefined` | Optional | Email addresses associated with the account |

## Example (as JSON)

```json
{
  "holders": [
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
      "relationship": "FOR_BENEFIT_OF_SECONDARY_JOINT_RESTRICTED"
    },
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
      "relationship": "FOR_BENEFIT_OF_SECONDARY_JOINT_RESTRICTED"
    }
  ],
  "emails": [
    "emails1"
  ]
}
```

