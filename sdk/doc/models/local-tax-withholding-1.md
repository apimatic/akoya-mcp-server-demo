
# Local Tax Withholding 1

Amount of local income tax withheld, if any

## Structure

`LocalTaxWithholding1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `taxWithheld` | `number \| undefined` | Optional | Amount of local income tax withheld |
| `localityName` | `string \| undefined` | Optional | Locality name |
| `income` | `number \| undefined` | Optional | Income amount for local tax purposes |

## Example (as JSON)

```json
{
  "taxWithheld": 15.4,
  "localityName": "localityName2",
  "income": 207.06
}
```

