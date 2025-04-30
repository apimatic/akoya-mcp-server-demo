
# State Tax Withholding

Income in a state and its tax withholding

## Structure

`StateTaxWithholding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `taxWithheld` | `number \| undefined` | Optional | Amount of state income tax withheld |
| `taxId` | `string \| undefined` | Optional | Filer's state tax id |
| `income` | `number \| undefined` | Optional | Income amount for state tax purposes |

## Example (as JSON)

```json
{
  "taxWithheld": 48.38,
  "taxId": "taxId0",
  "income": 15.96
}
```

