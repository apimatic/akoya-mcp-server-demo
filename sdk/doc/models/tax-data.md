
# Tax Data

Tax data container for API requests and responses

## Structure

`TaxData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `businessIncomeStatement` | [`BusinessIncomeStatement \| undefined`](../../doc/models/business-income-statement.md) | Optional | Business Income Statement for IRS Form 1040 Schedule C |
| `cryptocurrencyTaxStatement` | [`CryptocurrencyTaxStatementList1 \| undefined`](../../doc/models/cryptocurrency-tax-statement-list-1.md) | Optional | Cryptocurrency Tax Statement list |
| `farmIncomeStatement` | [`FarmIncomeStatement \| undefined`](../../doc/models/farm-income-statement.md) | Optional | Farm Income Statement for IRS Form 1040 Schedule F |
| `farmRentalIncomeStatement` | [`FarmRentalIncomeStatement \| undefined`](../../doc/models/farm-rental-income-statement.md) | Optional | Farm Rental Income Statement for IRS Form 4835 |
| `rentalIncomeStatement` | [`RentalIncomeStatement \| undefined`](../../doc/models/rental-income-statement.md) | Optional | Rental Income Statement for IRS Form 1040 Schedule E |
| `royaltyIncomeStatement` | [`RoyaltyIncomeStatement \| undefined`](../../doc/models/royalty-income-statement.md) | Optional | Royalty Income Statement for IRS Form 1040 Schedule E |
| `tax1041K1` | [`Form1041K12 \| undefined`](../../doc/models/form-1041-k12.md) | Optional | Beneficiary's Share of Income, Deductions, Credits, etc. |
| `tax1042S` | [`Form1042S2 \| undefined`](../../doc/models/form-1042-s2.md) | Optional | Foreign Person's U.S. Source Income Subject to Withholding |
| `tax1065K1` | [`Form1065K12 \| undefined`](../../doc/models/form-1065-k12.md) | Optional | Partner's Share of Income, Deductions, Credits, etc. |
| `tax1095A` | [`Form1095A2 \| undefined`](../../doc/models/form-1095-a2.md) | Optional | Health Insurance Marketplace Statement |
| `tax1095B` | [`Form1095B2 \| undefined`](../../doc/models/form-1095-b2.md) | Optional | Health Coverage |
| `tax1095C` | [`Form1095C2 \| undefined`](../../doc/models/form-1095-c2.md) | Optional | Employer-Provided Health Insurance Offer and Coverage |
| `tax1097Btc` | [`Form1097BTC2 \| undefined`](../../doc/models/form-1097-btc2.md) | Optional | Bond Tax Credit |
| `tax1098` | [`Form10982 \| undefined`](../../doc/models/form-10982.md) | Optional | Mortgage Interest Statement |
| `tax1098C` | [`Form1098C2 \| undefined`](../../doc/models/form-1098-c2.md) | Optional | Contributions of Motor Vehicles, Boats, and Airplanes |
| `tax1098E` | [`Form1098E2 \| undefined`](../../doc/models/form-1098-e2.md) | Optional | Student Loan Interest Statement |
| `tax1098Ma` | [`Form1098MA2 \| undefined`](../../doc/models/form-1098-ma2.md) | Optional | Mortgage Assistance Payments |
| `tax1098Q` | [`Form1098Q2 \| undefined`](../../doc/models/form-1098-q2.md) | Optional | Qualifying Longevity Annuity Contract Information |
| `tax1098T` | [`Form1098T2 \| undefined`](../../doc/models/form-1098-t2.md) | Optional | Tuition Statement |
| `tax1099A` | [`Form1099A2 \| undefined`](../../doc/models/form-1099-a2.md) | Optional | Acquisition or Abandonment of Secured Property |
| `tax1099B` | [`Form1099B2 \| undefined`](../../doc/models/form-1099-b2.md) | Optional | Proceeds From Broker and Barter Exchange Transactions |
| `tax1099C` | [`Form1099C2 \| undefined`](../../doc/models/form-1099-c2.md) | Optional | Cancellation of Debt |
| `tax1099Cap` | [`Form1099CAP2 \| undefined`](../../doc/models/form-1099-cap2.md) | Optional | Changes in Corporate Control and Capital Structure |
| `tax1099ConsolidatedStatement` | [`Form1099ConsolidatedStatement2 \| undefined`](../../doc/models/form-1099-consolidated-statement-2.md) | Optional | Consolidated Statement for combined IRS Form 1099s |
| `tax1099Div` | [`Form1099DIV2 \| undefined`](../../doc/models/form-1099-div2.md) | Optional | Dividends and Distributions |
| `tax1099G` | [`Form1099G2 \| undefined`](../../doc/models/form-1099-g2.md) | Optional | Certain Government Payments |
| `tax1099H` | [`Form1099H2 \| undefined`](../../doc/models/form-1099-h2.md) | Optional | Health Coverage Tax Credit (HCTC) Advance Payments |
| `tax1099Int` | [`Form1099INT2 \| undefined`](../../doc/models/form-1099-int2.md) | Optional | Interest Income |
| `tax1099K` | [`Form1099K2 \| undefined`](../../doc/models/form-1099-k2.md) | Optional | Merchant Card and Third-Party Network Payments |
| `tax1099Ls` | [`Form1099LS2 \| undefined`](../../doc/models/form-1099-ls2.md) | Optional | Reportable Life Insurance Sale |
| `tax1099Ltc` | [`Form1099LTC2 \| undefined`](../../doc/models/form-1099-ltc2.md) | Optional | Long-Term Care and Accelerated Death Benefits |
| `tax1099Misc` | [`Form1099MISC2 \| undefined`](../../doc/models/form-1099-misc2.md) | Optional | Miscellaneous Income |
| `tax1099Nec` | [`Form1099NEC2 \| undefined`](../../doc/models/form-1099-nec2.md) | Optional | Nonemployee Compensation |
| `tax1099Oid` | [`Form1099OID2 \| undefined`](../../doc/models/form-1099-oid2.md) | Optional | Original Issue Discount |
| `tax1099Patr` | [`Form1099PATR2 \| undefined`](../../doc/models/form-1099-patr2.md) | Optional | Taxable Distributions Received From Cooperatives |
| `tax1099Q` | [`Form1099Q2 \| undefined`](../../doc/models/form-1099-q2.md) | Optional | Payments From Qualified Education Programs |
| `tax1099Qa` | [`Form1099QA2 \| undefined`](../../doc/models/form-1099-qa2.md) | Optional | Distributions From ABLE Accounts |
| `tax1099R` | [`Form1099R2 \| undefined`](../../doc/models/form-1099-r2.md) | Optional | Distributions from Pensions, Annuities, Retirement or Profit-Sharing Plans, IRAs, Insurance Contracts, etc. |
| `tax1099S` | [`Form1099S2 \| undefined`](../../doc/models/form-1099-s2.md) | Optional | Proceeds From Real Estate Transactions |
| `tax1099Sa` | [`Form1099SA2 \| undefined`](../../doc/models/form-1099-sa2.md) | Optional | Distributions From an HSA, Archer MSA, or Medicare Advantage MSA |
| `tax1099Sb` | [`Form1099SB2 \| undefined`](../../doc/models/form-1099-sb2.md) | Optional | Seller's Investment in Life Insurance Contract |
| `tax1120SK1` | [`Form1120SK12 \| undefined`](../../doc/models/form-1120-sk12.md) | Optional | Shareholder's Share of Income, Deductions, Credits, etc. |
| `tax2439` | [`Form24392 \| undefined`](../../doc/models/form-24392.md) | Optional | Notice to Shareholder of Undistributed Long-Term Capital Gains |
| `tax3921` | [`Form39212 \| undefined`](../../doc/models/form-39212.md) | Optional | Exercise of an Incentive Stock Option Under Section 422(b) |
| `tax3922` | [`Form39222 \| undefined`](../../doc/models/form-39222.md) | Optional | Transfer of Stock Acquired Through an Employee Stock Purchase Plan under Section 423(c) |
| `tax5227K1` | [`Form1041K1 \| undefined`](../../doc/models/form-1041-k1.md) | Optional | Split-Interest Trust Beneficiary's schedule K-1 |
| `tax5498` | [`Form54982 \| undefined`](../../doc/models/form-54982.md) | Optional | IRA Contribution Information |
| `tax5498Esa` | [`Form5498ESA2 \| undefined`](../../doc/models/form-5498-esa2.md) | Optional | Coverdell ESA Contribution Information |
| `tax5498Qa` | [`Form5498QA2 \| undefined`](../../doc/models/form-5498-qa2.md) | Optional | ABLE Account Contribution Information |
| `tax5498Sa` | [`Form5498SA2 \| undefined`](../../doc/models/form-5498-sa2.md) | Optional | HSA, Archer MSA, or Medicare Advantage MSA Information |
| `taxW2` | [`FormW24 \| undefined`](../../doc/models/form-w24.md) | Optional | Wage and Tax Statement |
| `taxW2C` | [`FormW2c2 \| undefined`](../../doc/models/form-w2-c-2.md) | Optional | IRS form W-2c, Corrected Wage and Tax Statement |
| `taxW2G` | [`FormW2G2 \| undefined`](../../doc/models/form-w2-g2.md) | Optional | Certain Gambling Winnings |
| `taxRefundDirectDeposit` | [`TaxRefundDirectDeposit2 \| undefined`](../../doc/models/tax-refund-direct-deposit-2.md) | Optional | Tax refund direct deposit information |

## Example (as JSON)

```json
{
  "businessIncomeStatement": {
    "taxYear": 2018,
    "corrected": false,
    "accountId": "accountId4",
    "taxFormId": "taxFormId2",
    "taxFormDate": "2016-03-13T12:52:32.123Z"
  },
  "cryptocurrencyTaxStatement": {
    "taxYear": 2018,
    "corrected": false,
    "accountId": "accountId2",
    "taxFormId": "taxFormId0",
    "taxFormDate": "2016-03-13T12:52:32.123Z"
  },
  "farmIncomeStatement": {
    "taxYear": 2018,
    "corrected": false,
    "accountId": "accountId4",
    "taxFormId": "taxFormId2",
    "taxFormDate": "2016-03-13T12:52:32.123Z"
  },
  "farmRentalIncomeStatement": {
    "taxYear": 2018,
    "corrected": false,
    "accountId": "accountId8",
    "taxFormId": "taxFormId6",
    "taxFormDate": "2016-03-13T12:52:32.123Z"
  },
  "rentalIncomeStatement": {
    "taxYear": 2018,
    "corrected": false,
    "accountId": "accountId8",
    "taxFormId": "taxFormId6",
    "taxFormDate": "2016-03-13T12:52:32.123Z"
  }
}
```

