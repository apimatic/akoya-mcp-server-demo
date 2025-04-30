# Tax

Tax

```ts
const taxController = new TaxController(client);
```

## Class Name

`TaxController`

## Methods

* [Tax Forms Search](../../doc/controllers/tax.md#tax-forms-search)
* [Get Tax Form](../../doc/controllers/tax.md#get-tax-form)


# Tax Forms Search

Get the full lists of tax document data and tax form images available for a specific year for the current authorized customer.

```ts
async taxFormsSearch(
  version: VersionEnum,
  providerId: string,
  xAkoyaInteractionId?: string,
  xAkoyaInteractionType?: XAkoyaInteractionTypeEnum,
  accept?: AcceptEnum[],
  taxYear?: string,
  taxForms?: TypeFormTypeEnum[],
  accountId?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<TaxStatementList>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | [`VersionEnum`](../../doc/models/version-enum.md) | Template, Required | Endpoint version. |
| `providerId` | `string` | Template, Required | Provider to query for Tax data. |
| `xAkoyaInteractionId` | `string \| undefined` | Header, Optional | Unique identifier to associate with this request. No specific format required. |
| `xAkoyaInteractionType` | [`XAkoyaInteractionTypeEnum \| undefined`](../../doc/models/x-akoya-interaction-type-enum.md) | Header, Optional | Identifies whether the customer is present (USER) or it is a BATCH operation. Case-insensitive.<br><br>**Default**: `XAkoyaInteractionTypeEnum.User` |
| `accept` | [`AcceptEnum[] \| undefined`](../../doc/models/accept-enum.md) | Header, Optional | Use the [Accept HTTP request header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept) to indicate one or more content types to request for the search result response. Use `application/json` to request data or `application/pdf to request images in comma-separated array format. Use in combination with TaxDataTypeQuery parameter to request`application/json` responses in ''JSON'' or ''BASE64_PDF'' format for tax form data' |
| `taxYear` | `string \| undefined` | Query, Optional | Tax year in which to search for tax forms. |
| `taxForms` | [`TypeFormTypeEnum[] \| undefined`](../../doc/models/type-form-type-enum.md) | Query, Optional | One or more tax form type enums for the specific documents being requested. Comma separated |
| `accountId` | `string \| undefined` | Query, Optional | Unique account identifier (not the account number) |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [TaxStatementList](../../doc/models/tax-statement-list.md).

## Example Usage

```ts
const version = VersionEnum.V2;

const providerId = 'providerId6';

const xAkoyaInteractionId = 'unique-request-id-001';

const xAkoyaInteractionType = XAkoyaInteractionTypeEnum.User;

const accept: AcceptEnum[] = [
  AcceptEnum.EnumApplicationjson
];

const taxYear = '2024';

const taxForms: TypeFormTypeEnum[] = [
  TypeFormTypeEnum.Tax1099Div,
  TypeFormTypeEnum.Tax1099Int
];

try {
  const { result, ...httpResponse } = await taxController.taxFormsSearch(
  version,
  providerId,
  xAkoyaInteractionId,
  xAkoyaInteractionType,
  accept,
  taxYear,
  taxForms
);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

## Example Response *(as JSON)*

```json
{
  "ResultType lightweight Search Response with Forms 1099-DIV and 1099-INT": {
    "value": {
      "statements": [
        {
          "taxYear": 2020,
          "taxStatementId": "9876987698769876",
          "attributes": [
            {
              "name": "federalTaxWithheld",
              "value": "4014.00"
            }
          ],
          "taxDataType": "JSON",
          "forms": [
            {
              "tax1099Div": {
                "taxYear": 2020,
                "taxFormId": "9876987698769876",
                "taxFormDate": "2021-03-30",
                "additionalInformation": "FDX v6.0",
                "taxFormType": "Tax1099Div"
              }
            }
          ]
        },
        {
          "taxYear": 2020,
          "taxStatementId": "6543654365436543",
          "attributes": [
            {
              "name": "federalTaxWithheld",
              "value": "4011.00"
            }
          ],
          "taxDataType": "JSON",
          "forms": [
            {
              "tax1099Int": {
                "taxYear": 2020,
                "taxFormId": "6543654365436543",
                "taxFormDate": "2021-03-30",
                "additionalInformation": "FDX v6.0",
                "taxFormType": "Tax1099Int"
              }
            }
          ]
        }
      ]
    }
  },
  "ResultType details Search Response with Form 1098": null
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`CustomError`](../../doc/models/custom-error.md) |
| 404 | Not Found | [`CustomError`](../../doc/models/custom-error.md) |
| 405 | Method Not Allowed | `ApiError` |
| 406 | Not Acceptable | `ApiError` |
| 408 | Request timed out (round trip call took >10 seconds). | [`CustomError`](../../doc/models/custom-error.md) |
| 409 | Conflict | `ApiError` |
| 500 | Internal Server Error | [`CustomError`](../../doc/models/custom-error.md) |
| 501 | FDX Version Not Supported or Not Implemented | [`CustomError`](../../doc/models/custom-error.md) |
| 503 | Scheduled Maintenance | [`CustomError`](../../doc/models/custom-error.md) |


# Get Tax Form

Get the Tax Statement as JSON or PDF for a single tax document for the customer. Use [HTTP Accept request-header](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html) to specify desired content types. See `AcceptHeader` definition for typical values.

Not all providers support PDF payloads. See [this article](https://recipient.ddp.akoya.com/support/article/kA0Uw00000026VxKAI) in the Data Recipent Hub for a list of providers that support document PDFs.

```ts
async getTaxForm(
  version: VersionEnum,
  providerId: string,
  taxFormId: string,
  xAkoyaInteractionId?: string,
  xAkoyaInteractionType?: XAkoyaInteractionTypeEnum,
  taxDataType?: TypeDataTypeEnum,
  accept?: AcceptEnum[],
  requestOptions?: RequestOptions
): Promise<ApiResponse<TaxStatement1>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | [`VersionEnum`](../../doc/models/version-enum.md) | Template, Required | Endpoint version. |
| `providerId` | `string` | Template, Required | Provider to query for Tax data. |
| `taxFormId` | `string` | Template, Required | Unique identifier of the tax form to request. |
| `xAkoyaInteractionId` | `string \| undefined` | Header, Optional | Unique identifier to associate with this request. No specific format required. |
| `xAkoyaInteractionType` | [`XAkoyaInteractionTypeEnum \| undefined`](../../doc/models/x-akoya-interaction-type-enum.md) | Header, Optional | Identifies whether the customer is present (USER) or it is a BATCH operation. Case-insensitive.<br><br>**Default**: `XAkoyaInteractionTypeEnum.User` |
| `taxDataType` | [`TypeDataTypeEnum \| undefined`](../../doc/models/type-data-type-enum.md) | Query, Optional | Use taxDataType to request `application/json` tax form data response in 'JSON' or 'BASE64_PDF' format. Omit if either format is acceptable. Used in combination with AcceptHeader requesting `application/json` response |
| `accept` | [`AcceptEnum[] \| undefined`](../../doc/models/accept-enum.md) | Header, Optional | Use the [Accept HTTP request header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Accept) to indicate one or more content types to request for the search result response. Use `application/json` to request data or `application/pdf`to request images. In comma-separated array format.         Use in combination with TaxDataTypeQuery parameter to request `application/json` responses in ''JSON'' or ''BASE64_PDF'' format for tax form data' |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [TaxStatement1](../../doc/models/tax-statement-1.md).

## Example Usage

```ts
const version = VersionEnum.V2;

const providerId = 'providerId6';

const taxFormId = 'taxFormId2';

const xAkoyaInteractionId = 'unique-request-id-001';

const xAkoyaInteractionType = XAkoyaInteractionTypeEnum.User;

const taxDataType = TypeDataTypeEnum.JSON;

try {
  const { result, ...httpResponse } = await taxController.getTaxForm(
  version,
  providerId,
  taxFormId,
  xAkoyaInteractionId,
  xAkoyaInteractionType,
  taxDataType
);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch (error) {
  if (error instanceof ApiError) {
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

## Example Response *(as JSON)*

```json
{
  "taxYear": 2020,
  "taxStatementId": "1234123412341234",
  "attributes": [
    {
      "name": "Total tax withheld",
      "value": "8025.00"
    }
  ],
  "issuer": {
    "tin": "12-3456789",
    "partyType": "BUSINESS",
    "businessName": {
      "name1": "Financial Data Exchange"
    },
    "address": {
      "line1": "12020 Sunrise Valley Dr",
      "line2": "Suite 230",
      "city": "Reston",
      "region": "VA",
      "postalCode": "20191",
      "country": "US"
    },
    "phone": {
      "number": "8885551212"
    }
  },
  "recipient": {
    "tin": "xxx-xx-1234",
    "partyType": "INDIVIDUAL",
    "individualName": {
      "first": "Kris",
      "middle": "Q",
      "last": "Public"
    },
    "address": {
      "line1": "1 Main St",
      "city": "Melrose",
      "region": "NY",
      "postalCode": "12121",
      "country": "US"
    }
  },
  "taxDataType": "JSON",
  "forms": [
    {
      "tax1099Div": {
        "taxYear": 2020,
        "taxFormId": "9876987698769876",
        "taxFormDate": "2021-03-30",
        "additionalInformation": "FDX v6.0",
        "taxFormType": "Tax1099Div",
        "foreignAccountTaxCompliance": false,
        "accountNumber": "111-5555555",
        "ordinaryDividends": 1107,
        "qualifiedDividends": 1208,
        "totalCapitalGain": 2109,
        "unrecaptured1250Gain": 2210,
        "section1202Gain": 2311,
        "collectiblesGain": 2412,
        "nonTaxableDistribution": 3013,
        "federalTaxWithheld": 4014,
        "section199ADividends": 5015,
        "investmentExpenses": 6016,
        "foreignTaxPaid": 7017,
        "foreignCountry": "Mexico",
        "cashLiquidation": 9019,
        "nonCashLiquidation": 10020,
        "taxExemptInterestDividend": 11021,
        "specifiedPabInterestDividend": 12022,
        "stateAndLocal": [
          {
            "stateCode": "NY",
            "state": {
              "taxWithheld": 15023,
              "taxId": "14-000023"
            }
          }
        ]
      }
    },
    {
      "tax1099Int": {
        "taxYear": 2020,
        "taxFormId": "6543654365436543",
        "taxFormDate": "2021-03-30",
        "additionalInformation": "FDX v6.0",
        "taxFormType": "Tax1099Int",
        "foreignAccountTaxCompliance": false,
        "accountNumber": "111-5555555",
        "payerRtn": "007007007",
        "interestIncome": 1008,
        "earlyWithdrawalPenalty": 2009,
        "usBondInterest": 3010,
        "federalTaxWithheld": 4011,
        "investmentExpenses": 5012,
        "foreignTaxPaid": 6013,
        "foreignCountry": "Canada",
        "taxExemptInterest": 8015,
        "specifiedPabInterest": 9016,
        "marketDiscount": 10017,
        "bondPremium": 11018,
        "usBondPremium": 12019,
        "taxExemptBondPremium": 13020,
        "cusipNumber": "CUSIP",
        "stateAndLocal": [
          {
            "stateCode": "NY",
            "state": {
              "taxWithheld": 17022,
              "taxId": "15-000022"
            }
          }
        ]
      }
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Account ID is required for searching or validating authorization | [`CustomError`](../../doc/models/custom-error.md) |
| 404 | Tax Form for provided Tax Form ID was not found | [`CustomError`](../../doc/models/custom-error.md) |
| 405 | Method Not Allowed | `ApiError` |
| 406 | Content Type not Supported | [`CustomError`](../../doc/models/custom-error.md) |
| 408 | Request timed out (round trip call took >10 seconds). | [`CustomError`](../../doc/models/custom-error.md) |
| 409 | Tax forms are not currently available for this account or this year | [`CustomError`](../../doc/models/custom-error.md) |
| 500 | Catch-all exception where request was not processed due to an internal outage/issue. | [`CustomError`](../../doc/models/custom-error.md) |
| 501 | FdxVersion in header is not implemented. | [`CustomError`](../../doc/models/custom-error.md) |
| 503 | System is down for maintenance. | [`CustomError`](../../doc/models/custom-error.md) |

