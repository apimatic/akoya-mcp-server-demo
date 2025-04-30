# Balances

Balances

```ts
const balancesController = new BalancesController(client);
```

## Class Name

`BalancesController`


# Get-Balances

Account information that includes balances and rates of bank accounts, credit cards, loans, investments, and more.

To view the response schema, select the `200` response below. Then pick an option for annuity, deposit, insurance, investment, loan, and line of credit account types.

For an example payload response, see the `200` example response below the `Try it` feature. The example is from a deposit account but all account types are supported by this endpoint.

> 🛑
> 
> The *id_token* should be used as the bearer token with this call.

Use the `mode` query param to receive FDX-aligned, standardized data values (Beta). For example:

`https://sandbox-products.ddp.akoya.com/balances/v2/mikomo?mode=standard`

`mode` is available in both sandbox and production.

`mode` is supported by a subset of providers. Log into the [Data Recipient Hub](https://recipient.ddp.akoya.com/login) and click [here](https://recipient.ddp.akoya.com/support/article/kA0Uw00000015GzKAI) to view a list of all providers supporting the `mode` parameter.

```ts
async getBalances(
  version: string,
  providerId: string,
  xAkoyaInteractionType?: XAkoyaInteractionTypeEnum,
  mode?: ModeEnum,
  requestOptions?: RequestOptions
): Promise<ApiResponse<Balances>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `string` | Template, Required | Akoya major version number. Do not use minor version numbers. For instance, use v2 and not v2.2 |
| `providerId` | `string` | Template, Required | Id of provider |
| `xAkoyaInteractionType` | [`XAkoyaInteractionTypeEnum \| undefined`](../../doc/models/x-akoya-interaction-type-enum.md) | Header, Optional | Optional but recommended header to include with each data request.<br>Allowed values are `user` or `batch`.<br>`user` indicates a request is prompted by an end-user action.<br>`batch` indicates the request is part of a batch process. |
| `mode` | [`ModeEnum \| undefined`](../../doc/models/mode-enum.md) | Query, Optional | BETA. Default is raw. Use standard for FDX-aligned, standardized data values. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [Balances](../../doc/models/balances.md).

## Example Usage

```ts
const version = 'v2';

const providerId = 'mikomo';

const xAkoyaInteractionType = XAkoyaInteractionTypeEnum.Batch;

const mode = ModeEnum.Raw;

try {
  const { result, ...httpResponse } = await balancesController.getBalances(
  version,
  providerId,
  xAkoyaInteractionType,
  mode
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
  "accounts": [
    {
      "investmentAccount": {
        "accountId": "839502593",
        "accountType": "College Savings",
        "availableCashBalance": 0,
        "balanceAsOf": "2022-03-16T04:00:00Z",
        "balanceType": "ASSET",
        "currency": {
          "currencyCode": "USD"
        },
        "currentValue": 52672.49,
        "marginBalance": 0,
        "nickname": "529 for Kid"
      }
    },
    {
      "investmentAccount": {
        "accountId": "5426873",
        "accountNumberDisplay": "...7054",
        "accountType": "BROKERAGE",
        "allowedCheckWriting": false,
        "availableCashBalance": 0,
        "balanceList": [
          {
            "balanceDate": "2021-07-06",
            "balanceDescription": "Margin Call",
            "balanceName": "MARGINCALL",
            "balanceType": "AMOUNT",
            "balanceValue": 0,
            "currency": {
              "currencyCode": "USD"
            }
          },
          {
            "balanceDate": "2021-07-06",
            "balanceDescription": "Fed Call",
            "balanceName": "FEDCALL",
            "balanceType": "AMOUNT",
            "balanceValue": 0,
            "currency": {
              "currencyCode": "USD"
            }
          },
          {
            "balanceDate": "2021-07-06",
            "balanceDescription": "Intra Day",
            "balanceName": "INTRADAY",
            "balanceType": "AMOUNT",
            "balanceValue": 0,
            "currency": {
              "currencyCode": "USD"
            }
          },
          {
            "balanceDate": "2021-07-05",
            "balanceDescription": "Prior Day",
            "balanceName": "PRIORDAY",
            "balanceType": "AMOUNT",
            "balanceValue": 0,
            "currency": {
              "currencyCode": "USD"
            }
          }
        ],
        "currency": {
          "currencyCode": "USD"
        },
        "lastActivityDate": "2021-07-06T00:00:00Z",
        "margin": false,
        "marginBalance": 0,
        "nickname": "Self-Directed",
        "shortBalance": 0,
        "status": "OPEN",
        "transactionsIncluded": false
      }
    },
    {
      "depositAccount": {
        "accountId": "g833202fb0866d0ad83472c429",
        "accountNumberDisplay": "xxxxxxxx0071",
        "accountType": "CHECKING",
        "availableBalance": 106717.06,
        "balanceAsOf": "2022-04-24T14:15:22Z",
        "balanceType": "ASSET",
        "currency": {
          "currencyCode": "USD"
        },
        "currentBalance": 106717.06,
        "description": "Checking Plus",
        "fiAttributes": [
          {
            "name": "accountOpenedDate",
            "value": "2020-04-23"
          },
          {
            "name": "interestPaidLastYear",
            "value": "3.20"
          }
        ],
        "interestRate": 0.0125,
        "interestRateAsOf": "2022-04-24T14:15:22Z",
        "interestRateType": "FIXED",
        "interestYtd": 20.33,
        "lastActivityDate": "2022-04-24T14:15:22Z",
        "lineOfBusiness": "Personal",
        "nickname": "Nickname Checking Plus 0071",
        "productName": "Checking Plus",
        "status": "OPEN",
        "transferIn": true,
        "transferOut": true
      }
    },
    {
      "depositAccount": {
        "accountId": "5dbda8de96eeff05f23934523a1fc258",
        "accountNumberDisplay": "xxxx0134",
        "accountType": "CHECKING",
        "annualPercentageYield": 0,
        "availableBalance": 0,
        "balanceAsOf": "2022-04-24T14:15:22Z",
        "currency": {
          "currencyCode": "USD"
        },
        "currentBalance": 0,
        "description": "Virtual Wallet Student Reserve",
        "interestRateAsOf": "2022-04-24T14:15:22Z",
        "interestRateType": "FIXED",
        "lastActivityDate": "2022-04-01T10:05:00Z",
        "lineOfBusiness": "LBRB",
        "openingDayBalance": 0,
        "productName": "Virtual Wallet Student Reserve",
        "transactionsIncluded": false
      }
    },
    {
      "depositAccount": {
        "accountId": "11719ae5-2399-1278-e43c-43f24abb3058",
        "accountType": "CD",
        "annualPercentageYield": 0.75,
        "availableBalance": 6808.29,
        "balanceAsOf": "2021-04-07T10:20:43.276Z",
        "balanceType": "ASSET",
        "currency": {
          "currencyCode": "USD",
          "originalCurrencyCode": "USD"
        },
        "currentBalance": 6808.29,
        "description": "Certificate of Deposit",
        "fiAttributes": [
          {
            "name": "eStatements",
            "value": "False"
          },
          {
            "name": "interestPaidLastYear",
            "value": "50.72"
          },
          {
            "name": "isTransactionsSupported",
            "value": "False"
          },
          {
            "name": "issueDate",
            "value": "2019-03-21T00:00:00.000Z"
          },
          {
            "name": "interestPayoutFrequency",
            "value": "Semi-Annually (And At Maturity)"
          }
        ],
        "interestRate": 0.75,
        "interestYtd": 25.24,
        "lineOfBusiness": "CONSUMER",
        "maturityDate": "2024-03-21T00:00:00Z",
        "nickname": "Certificate of Deposit - 3691",
        "openingDayBalance": 2000,
        "parentAccountId": "11719ae5-2399-1278-e43c-43f24abb3058",
        "status": "OPEN",
        "term": 60,
        "transactionsIncluded": false,
        "transferIn": false,
        "transferOut": false
      }
    },
    {
      "depositAccount": {
        "accountId": "33fbd9e5-9cc3-3d7d-15b3-70d97d87ca1d",
        "accountType": "SAVINGS",
        "availableBalance": 20608.9,
        "balanceAsOf": "2021-04-07T10:08:11.833Z",
        "balanceType": "ASSET",
        "currency": {
          "currencyCode": "USD",
          "originalCurrencyCode": "USD"
        },
        "currentBalance": 20608.9,
        "description": "Savings",
        "fiAttributes": [
          {
            "name": "eStatements",
            "value": "True"
          }
        ],
        "interestRate": 0.01,
        "interestYtd": 0.29,
        "lineOfBusiness": "CONSUMER",
        "nickname": "Savings - 8537",
        "openingDayBalance": 20608.9,
        "parentAccountId": "33fbd9e5-9cc3-3d7d-15b3-70d97d87ca1d",
        "status": "OPEN",
        "transactionsIncluded": false
      }
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid Input | [`CustomError`](../../doc/models/custom-error.md) |
| 401 | Customer not authorized. | [`CustomError`](../../doc/models/custom-error.md) |
| 404 | 701 - Tax Lots not found. The `holdingId` may be wrong. | [`CustomError`](../../doc/models/custom-error.md) |
| 405 | Method Not Allowed | `ApiError` |
| 406 | Content Type not Supported | [`CustomError`](../../doc/models/custom-error.md) |
| 408 | Request timed out (round trip call took >10 seconds). | [`CustomError`](../../doc/models/custom-error.md) |
| 429 | 1207 - Too many requests | [`CustomError`](../../doc/models/custom-error.md) |
| 500 | Catch-all exception where request was not processed due to an internal outage/issue. | [`CustomError`](../../doc/models/custom-error.md) |
| 501 | FdxVersion in header is not implemented. | [`CustomError`](../../doc/models/custom-error.md) |
| 503 | System is down for maintenance. | [`CustomError`](../../doc/models/custom-error.md) |

