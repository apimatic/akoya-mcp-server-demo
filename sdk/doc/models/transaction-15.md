
# Transaction 15

## Structure

`Transaction15`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `depositTransaction` | [`DepositTransaction \| undefined`](../../doc/models/deposit-transaction.md) | Optional | Deposit transaction |
| `loanTransaction` | [`LoanTransaction \| undefined`](../../doc/models/loan-transaction.md) | Optional | Loan Transaction |
| `locTransaction` | [`LocTransaction \| undefined`](../../doc/models/loc-transaction.md) | Optional | A line of credit transaction of type |
| `investmentTransaction` | [`InvestmentTransaction \| undefined`](../../doc/models/investment-transaction.md) | Optional | Investment Transactions |
| `insuranceTransaction` | [`InsuranceTransaction \| undefined`](../../doc/models/insurance-transaction.md) | Optional | Insurance transactions |

## Example (as JSON)

```json
{
  "depositTransaction": {
    "accountId": "accountId0",
    "amount": 1.72,
    "category": "category8",
    "debitCreditMemo": "DEBIT",
    "description": "description0"
  },
  "loanTransaction": {
    "accountId": "accountId6",
    "amount": 163.78,
    "category": "category4",
    "debitCreditMemo": "DEBIT",
    "description": "description6"
  },
  "locTransaction": {
    "accountId": "accountId4",
    "amount": 130.76,
    "category": "category2",
    "debitCreditMemo": "DEBIT",
    "description": "description6"
  },
  "investmentTransaction": {
    "accountId": "accountId2",
    "amount": 139.34,
    "category": "category0",
    "debitCreditMemo": "DEBIT",
    "description": "description2"
  },
  "insuranceTransaction": {
    "accountId": "accountId4",
    "amount": 123.56,
    "category": "category2",
    "debitCreditMemo": "DEBIT",
    "description": "description6"
  }
}
```

