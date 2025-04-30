
# Loan Balances

Data elements included with balances specific to loan accounts

## Structure

`LoanBalances`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accountId` | `string \| undefined` | Optional | Long-term persistent identity of the account. Not an account number. This identity must be unique to the owning institution. |
| `accountType` | `string \| undefined` | Optional | The type of an account. For instance, CHECKING, SAVINGS, 401K, etc. |
| `accountNumberDisplay` | `string \| undefined` | Optional | Account display number for the end user’s handle at owning institution. This is to be displayed by the Interface Provider. |
| `currency` | [`CurrencyEntity \| undefined`](../../doc/models/currency-entity.md) | Optional | Indicates the currency code used by the account. May also include currency rate. |
| `description` | `string \| undefined` | Optional | - |
| `fiAttributes` | [`FiAttributeEntity[] \| undefined`](../../doc/models/fi-attribute-entity.md) | Optional | - |
| `nickname` | `string \| undefined` | Optional | Name given by the user. Used in UIs to assist in account selection |
| `productName` | `string \| undefined` | Optional | Marketed product name for this account.  Used in UIs to assist in account selection |
| `status` | [`StatusEnum \| undefined`](../../doc/models/status-enum.md) | Optional | The status of an account. |
| `lineOfBusiness` | `string \| undefined` | Optional | The line of business, such as consumer, consumer joint, small business, corporate, etc. |
| `balanceType` | [`BalanceTypeEnum \| undefined`](../../doc/models/balance-type-enum.md) | Optional | ASSET (positive transaction amount increases balance), LIABILITY (positive transaction amount decreases balance) |
| `interestRate` | `number \| undefined` | Optional | Interest Rate of Account |
| `interestRateType` | [`InterestRateTypeEnum \| undefined`](../../doc/models/interest-rate-type-enum.md) | Optional | The type of interest rate. FIXED or VARIABLE. |
| `interestRateAsOf` | `string \| undefined` | Optional | Date of account’s interest rate |
| `lastActivityDate` | `string \| undefined` | Optional | Date that last transaction occurred on account |
| `micrNumber` | `string \| undefined` | Optional | MICR Number |
| `parentAccountId` | `string \| undefined` | Optional | Long-term persistent identity of the parent account. This is used to group accounts. |
| `priorInterestRate` | `number \| undefined` | Optional | Previous Interest Rate of Account |
| `transferIn` | `boolean \| undefined` | Optional | Account is eligible for incoming transfers |
| `transferOut` | `boolean \| undefined` | Optional | Account is eligible for outgoing transfers |
| `compoundingPeriod` | [`CompoundingPeriodEnum \| undefined`](../../doc/models/compounding-period-enum.md) | Optional | - |
| `loanTerm` | `number \| undefined` | Optional | Term of loan in months |
| `maturityDate` | `string \| undefined` | Optional | Maturity date |
| `originatingDate` | `string \| undefined` | Optional | Loan origination date |
| `paymentFrequency` | [`PaymentFrequencyEnum \| undefined`](../../doc/models/payment-frequency-enum.md) | Optional | - |
| `totalNumberOfPayments` | `number \| undefined` | Optional | Total number of payments |
| `balanceAsOf` | `string \| undefined` | Optional | As-of date of balances |
| `escrowBalance` | `number \| undefined` | Optional | Escrow balance of loan |
| `interestPaidYearToDate` | `number \| undefined` | Optional | Interest paid year to date |
| `lastPaymentAmount` | `number \| undefined` | Optional | Last payment amount |
| `lastPaymentDate` | `string \| undefined` | Optional | Last payment date |
| `nextPaymentAmount` | `number \| undefined` | Optional | Amount of next payment |
| `nextPaymentDate` | `string \| undefined` | Optional | Date of next payment |
| `originalPrincipal` | `number \| undefined` | Optional | Original principal of loan |
| `payOffAmount` | `number \| undefined` | Optional | Payoff amount |
| `principalBalance` | `number \| undefined` | Optional | Principal balance of loan |

## Example (as JSON)

```json
{
  "accountId": "accountId8",
  "accountType": "accountType8",
  "accountNumberDisplay": "accountNumberDisplay4",
  "currency": {
    "currencyCode": "currencyCode0",
    "currencyRate": 27.48,
    "originalCurrencyCode": "originalCurrencyCode4"
  },
  "description": "description8"
}
```

