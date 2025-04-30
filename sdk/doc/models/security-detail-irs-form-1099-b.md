
# Security Detail IRS Form 1099 B

Tax information for a single security transaction

## Structure

`SecurityDetailIRSForm1099B`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `checkboxOnForm8949` | `string \| undefined` | Optional | Applicable checkbox on Form 8949 |
| `securityName` | `string \| undefined` | Optional | Security name |
| `numberOfShares` | `number \| undefined` | Optional | Number of shares |
| `saleDescription` | `string \| undefined` | Optional | Box 1a, Description of property |
| `dateAcquired` | `string \| undefined` | Optional | Box 1b, Date acquired |
| `variousDatesAcquired` | `boolean \| undefined` | Optional | Box 1b, Date acquired Various |
| `dateOfSale` | `string \| undefined` | Optional | Box 1c, Date sold or disposed |
| `salesPrice` | `number \| undefined` | Optional | Box 1d, Proceeds (not price per share) |
| `accruedMarketDiscount` | `number \| undefined` | Optional | Box 1f, Accrued market discount |
| `adjustmentCodes` | [`CodeAndAmount[] \| undefined`](../../doc/models/code-and-amount.md) | Optional | Other adjustments (code and amount) |
| `costBasis` | `number \| undefined` | Optional | Box 1e, Cost or other basis |
| `correctedCostBasis` | `number \| undefined` | Optional | Corrected cost basis. May be supplied in lieu of adjustmentCode code B. If both adjustmentCodes and correctedCostBasis are supplied, costBasis plus adjustmentCode B should equal correctedCostBasis |
| `washSaleLossDisallowed` | `number \| undefined` | Optional | Box 1g, Wash sale loss disallowed |
| `longOrShort` | [`SaleTermType2Enum \| undefined`](../../doc/models/sale-term-type-2-enum.md) | Optional | Box 2, LONG or SHORT |
| `ordinary` | `boolean \| undefined` | Optional | Box 2, Ordinary |
| `collectible` | `boolean \| undefined` | Optional | Box 3, Collectibles |
| `qof` | `boolean \| undefined` | Optional | Box 3, Qualified Opportunity Fund (QOF) |
| `federalTaxWithheld` | `number \| undefined` | Optional | Box 4, Federal income tax withheld |
| `noncoveredSecurity` | `boolean \| undefined` | Optional | Box 5, Noncovered security |
| `grossOrNet` | [`SaleProceedsType1Enum \| undefined`](../../doc/models/sale-proceeds-type-1-enum.md) | Optional | Box 6, Reported to IRS: GROSS or NET |
| `lossNotAllowed` | `boolean \| undefined` | Optional | Box 7, Loss not allowed based on proceeds |
| `basisReported` | `boolean \| undefined` | Optional | Box 12, Basis reported to IRS |
| `stateAndLocal` | [`StateAndLocalTaxWithholding[] \| undefined`](../../doc/models/state-and-local-tax-withholding.md) | Optional | Boxes 14-16, State and Local tax withholding |
| `cusip` | `string \| undefined` | Optional | CUSIP number |
| `foreignAccountTaxCompliance` | `boolean \| undefined` | Optional | Foreign account tax compliance |
| `expiredOption` | [`ExpiredOptionType1Enum \| undefined`](../../doc/models/expired-option-type-1-enum.md) | Optional | To indicate gain or loss resulted from option expiration. If salesPrice (1d, proceeds) is zero, use PURCHASED. If costBasis (1e) is zero, use GRANTED |
| `investmentSaleType` | [`InvestmentSaleTypeEnum \| undefined`](../../doc/models/investment-sale-type-enum.md) | Optional | Type of investment sale |

## Example (as JSON)

```json
{
  "dateAcquired": "2021-07-15",
  "dateOfSale": "2021-07-15",
  "checkboxOnForm8949": "checkboxOnForm89498",
  "securityName": "securityName6",
  "numberOfShares": 126.44,
  "saleDescription": "saleDescription4"
}
```

