
# Tax Form Attribute

An additional tax form attribute for use when a defined field is not available

## Structure

`TaxFormAttribute`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | Name of attribute |
| `value` | `string \| undefined` | Optional | Value of attribute |
| `boxNumber` | `string \| undefined` | Optional | Box number on a tax form, if any |
| `code` | `string \| undefined` | Optional | Tax form code for the given box number, if any |

## Example (as JSON)

```json
{
  "name": "name2",
  "value": "value4",
  "boxNumber": "boxNumber0",
  "code": "code0"
}
```

