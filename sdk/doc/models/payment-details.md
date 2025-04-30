
# Payment Details

Payment details for some transactions

## Structure

`PaymentDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `escrowAmount` | `number \| undefined` | Optional | The amount of payment applied to escrow |
| `feesAmount` | `number \| undefined` | Optional | The amount of payment applied to fees |
| `insuranceAmount` | `number \| undefined` | Optional | The amount of payment applied to life/health/accident insurance on the loan |
| `interestAmount` | `number \| undefined` | Optional | The amount of payment applied to interest |
| `pmiAmount` | `number \| undefined` | Optional | The amount of payment applied to PMI |
| `principalAmount` | `number \| undefined` | Optional | The amount of payment applied to principal |

## Example (as JSON)

```json
{
  "escrowAmount": 171.3,
  "feesAmount": 83.52,
  "insuranceAmount": 63.4,
  "interestAmount": 64.72,
  "pmiAmount": 217.98
}
```

