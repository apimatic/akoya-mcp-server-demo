
# Health Insurance Covered Individual

Used on Form 1095-B Part IV and Form 1095-C Part III

## Structure

`HealthInsuranceCoveredIndividual`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | [`IndividualName1 \| undefined`](../../doc/models/individual-name-1.md) | Optional | Name of responsible individual |
| `tin` | `string \| undefined` | Optional | Social security number or other TIN |
| `dateOfBirth` | `string \| undefined` | Optional | Date of birth |
| `coveredAll12Months` | `boolean \| undefined` | Optional | Covered all 12 months |
| `coveredMonths` | [`MonthAbbreviationEnum[] \| undefined`](../../doc/models/month-abbreviation-enum.md) | Optional | Months covered |

## Example (as JSON)

```json
{
  "dateOfBirth": "2021-07-15",
  "name": {
    "first": "first6",
    "middle": "middle6",
    "last": "last0",
    "suffix": "suffix0"
  },
  "tin": "tin4",
  "coveredAll12Months": false,
  "coveredMonths": [
    "FEB",
    "MAR"
  ]
}
```

