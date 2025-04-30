
# Health Insurance Coverage

Used on Form 1095-A Part III

## Structure

`HealthInsuranceCoverage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enrollmentPremium` | `number \| undefined` | Optional | Monthly enrollment premiums |
| `slcspPremium` | `number \| undefined` | Optional | Monthly second lowest cost silver plan (SLCSP) premium |
| `advancePremiumTaxCreditPayment` | `number \| undefined` | Optional | Monthly advance payment of premium tax credit |
| `month` | [`CoverageMonth1Enum \| undefined`](../../doc/models/coverage-month-1-enum.md) | Optional | Month of coverage |

## Example (as JSON)

```json
{
  "enrollmentPremium": 139.74,
  "slcspPremium": 163.34,
  "advancePremiumTaxCreditPayment": 197.06,
  "month": "MAY"
}
```

