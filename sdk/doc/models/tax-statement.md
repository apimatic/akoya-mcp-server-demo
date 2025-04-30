
# Tax Statement

Tax statement containing one or more tax forms

## Structure

`TaxStatement`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `taxYear` | `number \| undefined` | Optional | Year for which taxes are being paid<br><br>**Constraints**: `>= 2018`, `<= 2050` |
| `taxStatementId` | `string \| undefined` | Optional | Long-term persistent id for the tax statement. Depending upon the data provider, this may be the same id as the id on the enclosed tax form(s), or this may be a different id |
| `issuer` | [`TaxParty6 \| undefined`](../../doc/models/tax-party-6.md) | Optional | Issuer's name, address, phone, and TIN. Issuer data need only be transmittted on TaxStatement, 'JSON' data type responses if it is the same on all included tax forms |
| `recipient` | [`TaxParty7 \| undefined`](../../doc/models/tax-party-7.md) | Optional | Recipient's name, address, phone, and TIN. Recipient data need only be transmittted on TaxStatement, 'JSON' data type responses if it is the same on all included tax forms |
| `taxDataType` | [`TypeDataType1Enum \| undefined`](../../doc/models/type-data-type-1-enum.md) | Optional | Whether this `application/json` tax form response contains data in `forms` property (as 'JSON' format) or `pdf` property (as 'BASE64_PDF' format) |
| `forms` | [`TaxData[] \| undefined`](../../doc/models/tax-data.md) | Optional | The list of data contents for all included tax forms, response should include one of `forms` or `pdf` |
| `pdf` | `string \| undefined` | Optional | PDF version of the tax statement containing all form pages, binary encoded as Base64, response should include one of `pdf` or `forms` |
| `attributes` | [`FiAttributeEntity[] \| undefined`](../../doc/models/fi-attribute-entity.md) | Optional | Additional tax statement attributes that the provider wishes to include |

## Example (as JSON)

```json
{
  "taxYear": 2023,
  "taxStatementId": "taxStatementId0",
  "issuer": {
    "tin": "tin0",
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
  },
  "recipient": {
    "tin": "tin2",
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
  },
  "taxDataType": "BASE64_PDF"
}
```

