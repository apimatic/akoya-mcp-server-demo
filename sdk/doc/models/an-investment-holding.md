
# An Investment Holding

## Structure

`AnInvestmentHolding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assetClasses` | [`AssetClass[] \| undefined`](../../doc/models/asset-class.md) | Optional | Percent breakdown by asset class.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `averageCost` | `boolean \| undefined` | Optional | Cost is average of all purchases for holding. |
| `cashAccount` | `boolean \| undefined` | Optional | If true, indicates that this holding is used to maintain proceeds from sales, dividends, and other cash postings to the investment account. |
| `changeInPrice` | `number \| undefined` | Optional | Change in current price compared to previous day's close |
| `currency` | [`CurrencyEntity \| undefined`](../../doc/models/currency-entity.md) | Optional | Indicates the currency code used by the account. May also include currency rate. |
| `currentUnitPrice` | `number \| undefined` | Optional | - |
| `currentUnitPriceDate` | `string \| undefined` | Optional | Current unit price as of date |
| `description` | `string \| undefined` | Optional | Description of the holding |
| `expirationDate` | `string \| undefined` | Optional | For CDs, bonds, and other time-based holdings. |
| `faceValue` | `number \| undefined` | Optional | Face value at the time of data retrieved. |
| `fiAssetClasses` | [`FiAssetClass[] \| undefined`](../../doc/models/fi-asset-class.md) | Optional | Percent breakdown by FI-specific asset class percentage breakdown |
| `fiAttributes` | [`FiAttributeEntity[] \| undefined`](../../doc/models/fi-attribute-entity.md) | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `heldInAccount` | [`HeldInAccountEnum \| undefined`](../../doc/models/held-in-account-enum.md) | Optional | Sub-account |
| `holdingId` | `string \| undefined` | Optional | Long term persistent identity of the holding |
| `holdingName` | `string \| undefined` | Optional | Holding name or security name |
| `holdingSubType` | [`HoldingSubTypeEnum \| undefined`](../../doc/models/holding-sub-type-enum.md) | Optional | - |
| `holdingType` | [`HoldingTypeEnum \| undefined`](../../doc/models/holding-type-enum.md) | Optional | - |
| `inv401kSurce` | [`Inv401kSurceEnum \| undefined`](../../doc/models/inv-401-k-surce-enum.md) | Optional | Source for money for this security. |
| `marketValue` | `number \| undefined` | Optional | Market value at the time of data retrieved |
| `originalPurchaseDate` | `string \| undefined` | Optional | Date of original purchase |
| `positionType` | [`PositionTypeEnum \| undefined`](../../doc/models/position-type-enum.md) | Optional | - |
| `purchasedPrice` | `number \| undefined` | Optional | Price of holding at the time of purchase |
| `rate` | `number \| undefined` | Optional | For CDs, bonds, and other rate based holdings. |
| `securityId` | `string \| undefined` | Optional | Unique identifier of security |
| `securityIdType` | [`SecurityIdTypeEnum \| undefined`](../../doc/models/security-id-type-enum.md) | Optional | Security identifier type |
| `symbol` | `string \| undefined` | Optional | Ticker / Market symbol |
| `taxLots` | [`TaxLot[] \| undefined`](../../doc/models/tax-lot.md) | Optional | Breakdown by tax lot.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `units` | `number \| undefined` | Optional | Number of shares (with decimals). |
| `mutualFundSecurity` | [`MutualFundSecurityEntity \| undefined`](../../doc/models/mutual-fund-security-entity.md) | Optional | Information about the mutual fund security specific to the type of security |
| `optionSecurity` | [`OptionSecurityEntity \| undefined`](../../doc/models/option-security-entity.md) | Optional | Information about the option security specific to the type of security |
| `otherSecurity` | [`OtherSecurityEntity \| undefined`](../../doc/models/other-security-entity.md) | Optional | Information about the security specific to the type of security |
| `stockSecurity` | [`StockSecurityEntity \| undefined`](../../doc/models/stock-security-entity.md) | Optional | Information about the stock security specific to the type of security |
| `sweepSecurity` | [`SweepSecurityEntity \| undefined`](../../doc/models/sweep-security-entity.md) | Optional | Information about the sweep security specific to the type of security |
| `debtSecurity` | [`DebtSecurityEntity \| undefined`](../../doc/models/debt-security-entity.md) | Optional | Information about the debt security specific to the type of security |

## Example (as JSON)

```json
{
  "assetClasses": [
    {
      "assetClass": "DOMESTICBOND",
      "percent": 174.1
    },
    {
      "assetClass": "DOMESTICBOND",
      "percent": 174.1
    }
  ],
  "averageCost": false,
  "cashAccount": false,
  "changeInPrice": 26.72,
  "currency": {
    "currencyCode": "currencyCode0",
    "currencyRate": 27.48,
    "originalCurrencyCode": "originalCurrencyCode4"
  }
}
```

