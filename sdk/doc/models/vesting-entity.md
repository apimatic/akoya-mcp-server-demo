
# Vesting Entity

Provides the past, present, and future vesting schedule and percentages.

## Structure

`VestingEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vestingDate` | `string \| undefined` | Optional | Vesting date |
| `symbol` | `string \| undefined` | Optional | Security symbol |
| `strikePrice` | `number \| undefined` | Optional | Strike price |
| `vestingPercentage` | `number \| undefined` | Optional | Vesting percentage |
| `otherVestAmount` | `number \| undefined` | Optional | Other vest amount |
| `otherVestPercentage` | `number \| undefined` | Optional | Other vest percentage |
| `vestedBalance` | `number \| undefined` | Optional | Vested balance |
| `unVestedBalance` | `number \| undefined` | Optional | Unvested balance |
| `vestedQuantity` | `number \| undefined` | Optional | Vested qualtity |
| `unVestedQuantity` | `number \| undefined` | Optional | Unvested quantity |

## Example (as JSON)

```json
{
  "vestingDate": "2016-03-13T12:52:32.123Z",
  "symbol": "symbol0",
  "strikePrice": 216.86,
  "vestingPercentage": 250.28,
  "otherVestAmount": 111.28
}
```

