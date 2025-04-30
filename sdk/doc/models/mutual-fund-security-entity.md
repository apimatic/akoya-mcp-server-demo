
# Mutual Fund Security Entity

Information about the mutual fund security specific to the type of security

## Structure

`MutualFundSecurityEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mutualFundType` | [`MutualFundTypeEnum \| undefined`](../../doc/models/mutual-fund-type-enum.md) | Optional | Mutual fund type |
| `unitsStreet` | `number \| undefined` | Optional | Units in the FI's street name, positive quantity |
| `unitsUser` | `number \| undefined` | Optional | Units in user's name directly, positive  quantity |
| `reinvestDividends` | `boolean \| undefined` | Optional | Reinvest dividends |
| `reinvestCapitalGains` | `boolean \| undefined` | Optional | Reinvest capital gains |
| `yield` | `number \| undefined` | Optional | Current yield reported as portion of the fund's assets |
| `yieldAsOfDate` | `string \| undefined` | Optional | As-of date for yield value |

## Example (as JSON)

```json
{
  "mutualFundType": "OPENEND",
  "unitsStreet": 101.68,
  "unitsUser": 108.4,
  "reinvestDividends": false,
  "reinvestCapitalGains": false
}
```

