
# Address 2

## Structure

`Address2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type1Enum \| undefined`](../../doc/models/type-1-enum.md) | Optional | The location type of an address |
| `line1` | `string \| undefined` | Optional | May contain full address if not separated |
| `line2` | `string \| undefined` | Optional | - |
| `line3` | `string \| undefined` | Optional | - |
| `city` | `string \| undefined` | Optional | - |
| `state` | `string \| undefined` | Optional | - |
| `postalCode` | `string \| undefined` | Optional | - |
| `country` | `string \| undefined` | Optional | ISO 3166 Country Code |

## Example (as JSON)

```json
{
  "type": "MAILING",
  "line1": "line12",
  "line2": "line24",
  "line3": "line32",
  "city": "city0"
}
```

