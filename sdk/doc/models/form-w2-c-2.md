
# Form W2 C 2

IRS form W-2c, Corrected Wage and Tax Statement

## Structure

`FormW2c2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `taxYear` | `number \| undefined` | Optional | Year for which taxes are being paid<br><br>**Constraints**: `>= 2018`, `<= 2050` |
| `corrected` | `boolean \| undefined` | Optional | True to indicate this is a corrected tax form |
| `accountId` | `string \| undefined` | Optional | Long-term persistent identity of the source account. Not the account number |
| `taxFormId` | `string \| undefined` | Optional | Long-term persistent id for this tax form. Depending upon the data provider, this may be the same id as the enclosing tax statement id, or this may be a different id, or this id may be omitted. |
| `taxFormDate` | `string \| undefined` | Optional | Date of production or delivery of the tax form |
| `additionalInformation` | `string \| undefined` | Optional | Additional explanation text or content about this tax form |
| `taxFormType` | [`TypeFormType2Enum \| undefined`](../../doc/models/type-form-type-2-enum.md) | Optional | Enumerated name of the tax form entity e.g. "TaxW2" |
| `issuer` | [`TaxParty8 \| undefined`](../../doc/models/tax-party-8.md) | Optional | Issuer's name, address, phone, and TIN. Issuer data need only be transmitted on enclosing TaxStatement, if it is the same on all its included tax forms. |
| `recipient` | [`TaxParty1 \| undefined`](../../doc/models/tax-party-1.md) | Optional | Recipient's name, address, phone, and TIN. Recipient data need only be transmitted on enclosing TaxStatement, if it is the same on all its included tax forms. |
| `attributes` | [`TaxFormAttribute[] \| undefined`](../../doc/models/tax-form-attribute.md) | Optional | Additional attributes for this tax form when defined fields are not available. Some specific additional attributes already defined by providers: Fields required by [IRS FIRE](https://www.irs.gov/e-file-providers/filing-information-returns-electronically-fire): Name Control, Type of Identification Number (EIN, SSN, ITIN, ATIN). (ATIN is tax ID number for pending adoptions.) Tax form provider field for taxpayer notification: Recipient Email Address. |
| `error` | [`Error2 \| undefined`](../../doc/models/error-2.md) | Optional | Present if an error was encountered while retrieving this form |
| `links` | [`HATEOASLink[] \| undefined`](../../doc/models/hateoas-link.md) | Optional | Links to retrieve this form as data or image, or to invoke other APIs |
| `correctedTinOrName` | `boolean \| undefined` | Optional | Box e, Corrected SSN and/or name |
| `previousEmployeeTin` | `string \| undefined` | Optional | Box f, Employee's previously reported SSN |
| `previousEmployeeName` | [`IndividualName3 \| undefined`](../../doc/models/individual-name-3.md) | Optional | Box g, Employee's previously reported name |
| `originalW2` | [`FormW21 \| undefined`](../../doc/models/form-w21.md) | Optional | Boxes 1-20 of Previously reported Wage and Tax Statement |
| `correctedW2` | [`FormW22 \| undefined`](../../doc/models/form-w22.md) | Optional | Boxes 1-20 of Correct information Wage and Tax Statement |

## Example (as JSON)

```json
{
  "taxYear": 2023,
  "taxFormDate": "2021-07-15",
  "attributes": [
    {
      "name": "nameControl",
      "value": "WILC"
    },
    {
      "name": "recipientIdType",
      "value": "EIN",
      "code": "1"
    },
    {
      "name": "recipientIdType",
      "value": "SSN",
      "code": "2"
    },
    {
      "name": "recipientIdType",
      "value": "ITIN",
      "code": "2"
    },
    {
      "name": "recipientIdType",
      "value": "ATIN",
      "code": "2"
    }
  ],
  "corrected": false,
  "accountId": "accountId6",
  "taxFormId": "taxFormId4"
}
```

