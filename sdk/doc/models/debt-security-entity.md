
# Debt Security Entity

Information about the debt security specific to the type of security

## Structure

`DebtSecurityEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `parValue` | `number \| undefined` | Optional | Par value amount |
| `debtType` | [`DebtTypeEnum \| undefined`](../../doc/models/debt-type-enum.md) | Optional | Debt type |
| `debtClass` | [`DebtClassEnum \| undefined`](../../doc/models/debt-class-enum.md) | Optional | Classification of debt |
| `couponRate` | `number \| undefined` | Optional | Bond coupon rate for next closest call date |
| `couponDate` | `string \| undefined` | Optional | Maturity date for next coupon |
| `couponMatureFrequency` | [`CouponMatureFrequencyEnum \| undefined`](../../doc/models/coupon-mature-frequency-enum.md) | Optional | When coupons mature |
| `callPrice` | `number \| undefined` | Optional | Bond call price |
| `yieldToCall` | `number \| undefined` | Optional | Yield to next call |
| `callDate` | `string \| undefined` | Optional | Next call date |
| `callType` | [`CallTypeEnum \| undefined`](../../doc/models/call-type-enum.md) | Optional | Type of next call |
| `yieldToMaturity` | `number \| undefined` | Optional | Yield to maturity |
| `bondMaturityDate` | `string \| undefined` | Optional | Bond Maturity date |

## Example (as JSON)

```json
{
  "parValue": 18.14,
  "debtType": "ASSET",
  "debtClass": "CORPORATE",
  "couponRate": 229.02,
  "couponDate": "2016-03-13T12:52:32.123Z"
}
```

