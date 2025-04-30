
# Customer 1

Represents a customer (end-user)

## Structure

`Customer1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `customerId` | `string \| undefined` | Optional | Long-term persistent identity of the end-user. This identity must be unique to the owning institution |
| `name` | [`Name \| undefined`](../../doc/models/name.md) | Optional | The end-user's name |
| `addresses` | [`Address2[] \| undefined`](../../doc/models/address-2.md) | Optional | An array of the end-user's physical mail addresses<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `telephones` | [`Telephone[] \| undefined`](../../doc/models/telephone.md) | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `email` | `string[] \| undefined` | Optional | An array of the end-user's electronic mail addresses |
| `accounts` | [`Account8[] \| undefined`](../../doc/models/account-8.md) | Optional | List of accounts related to this end-user<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |

## Example (as JSON)

```json
{
  "customerId": "customerId2",
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
    },
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
    }
  ],
  "email": [
    "email0",
    "email1"
  ]
}
```

