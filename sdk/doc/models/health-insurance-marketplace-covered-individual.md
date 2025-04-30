
# Health Insurance Marketplace Covered Individual

Used on Form 1095-A Part II

## Structure

`HealthInsuranceMarketplaceCoveredIndividual`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | Covered individual name |
| `tin` | `string \| undefined` | Optional | Covered individual SSN |
| `dateOfBirth` | `string \| undefined` | Optional | Covered individual date of birth |
| `policyStartDate` | `string \| undefined` | Optional | Coverage start date |
| `policyTerminationDate` | `string \| undefined` | Optional | Coverage termination date |

## Example (as JSON)

```json
{
  "dateOfBirth": "2021-07-15",
  "policyStartDate": "2021-07-15",
  "policyTerminationDate": "2021-07-15",
  "name": "name2",
  "tin": "tin8"
}
```

