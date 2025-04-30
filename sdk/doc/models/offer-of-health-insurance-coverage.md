
# Offer of Health Insurance Coverage

Health insurance coverage offer for part II of IRS Form 1095-C

## Structure

`OfferOfHealthInsuranceCoverage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `coverageCode` | `string \| undefined` | Optional | Offer of Coverage (enter required code) |
| `requiredContribution` | `number \| undefined` | Optional | Employee required contribution |
| `section4980HCode` | `string \| undefined` | Optional | Section 4980H Safe Harbor and Other Relief (enter code) |
| `postalCode` | `string \| undefined` | Optional | Box 17, ZIP Code<br><br>**Constraints**: *Maximum Length*: `10` |
| `month` | [`CoverageMonth2Enum \| undefined`](../../doc/models/coverage-month-2-enum.md) | Optional | Month |

## Example (as JSON)

```json
{
  "coverageCode": "coverageCode8",
  "requiredContribution": 234.32,
  "section4980HCode": "section4980HCode4",
  "postalCode": "postalCode2",
  "month": "NOVEMBER"
}
```

