
# Form 1042 S Agent 1

Boxes 12a-i, Withholding agent

## Structure

`Form1042SAgent1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tin` | `string \| undefined` | Optional | Issuer or recipient Tax Identification Number. Usually EIN for issuer and SSN for recipient |
| `partyType` | [`TaxPartyType2Enum \| undefined`](../../doc/models/tax-party-type-2-enum.md) | Optional | Type of issuer or recipient legal entity, as "BUSINESS" or "INDIVIDUAL". Commonly BUSINESS for issuer and INDIVIDUAL for recipient |
| `individualName` | [`IndividualName4 \| undefined`](../../doc/models/individual-name-4.md) | Optional | Individual issuer or recipient name |
| `businessName` | [`BusinessName1 \| undefined`](../../doc/models/business-name-1.md) | Optional | Business issuer or recipient name |
| `address` | [`Address1 \| undefined`](../../doc/models/address-1.md) | Optional | Issuer or recipient address |
| `phone` | [`TelephoneNumberPlusExtension4 \| undefined`](../../doc/models/telephone-number-plus-extension-4.md) | Optional | Issuer or recipient telephone number |
| `email` | `string \| undefined` | Optional | Issuer or recipient email address. (Additional information, not part of IRS forms) |
| `ch3StatusCode` | `string \| undefined` | Optional | Ch. 3 status code,<br><br>* Box 12b, Withholding Agent,<br>* Box 13f, Recipient,<br>* Box 15b, Intermediary or flow-through entity,<br>* Box 16d, Payer |
| `ch4StatusCode` | `string \| undefined` | Optional | Ch. 4 status code,<br><br>* Box 12c, Withholding Agent,<br>* Box 13g, Recipient,<br>* Box 15c, Intermediary or flow-through entity,<br>* Box 16e, Payer |
| `giin` | `string \| undefined` | Optional | Agent's Global Intermediary Identification Number (GIIN),<br><br>* Box 12e, Withholding Agent,<br>* Box 13h, Recipient,<br>* Box 15e, Intermediary or flow-through entity,<br>* Box 16c, Payer |
| `foreignTin` | `string \| undefined` | Optional | Foreign tax identification number, if any,<br><br>* Box 12g, Withholding Agent,<br>* Box 13i, Recipient,<br>* Box 15g, Intermediary or flow-through entity |

## Example (as JSON)

```json
{
  "tin": "tin6",
  "partyType": "BUSINESS",
  "individualName": {
    "first": "first0",
    "middle": "middle0",
    "last": "last4",
    "suffix": "suffix4"
  },
  "businessName": {
    "name1": "name18",
    "name2": "name22"
  },
  "address": {
    "line1": "line18",
    "line2": "line20",
    "line3": "line38",
    "city": "city6",
    "region": "region2"
  }
}
```

