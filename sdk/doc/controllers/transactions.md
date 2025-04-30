# Transactions

Transactions

```ts
const transactionsController = new TransactionsController(client);
```

## Class Name

`TransactionsController`


# Get-Transactions

The transactions API allows you to retrieve transaction history of consumer-permissioned accounts.

> 🛑
> 
> The *id_token* should be used as the bearer token with this call.

For more information on how to paginate transaction results, please see: [Pagination](https://docs.akoya.com/v2/docs/pagination)

Use the `mode` query param to receive FDX-aligned, standardized data values (Beta). For example:

`https://sandbox-products.ddp.akoya.com/transactions/v2/mikomo?mode=standard`

`mode` is available in both sandbox and production.

`mode` is supported by a subset of providers. Log into the [Data Recipient Hub](https://recipient.ddp.akoya.com/login) and click [here](https://recipient.ddp.akoya.com/support/article/kA0Uw00000015GzKAI) to view a list of all providers supporting the `mode` parameter.

```ts
async getTransactions(
  version: string,
  providerId: string,
  accountId: string,
  startTime?: string,
  endTime?: string,
  offset?: string,
  limit?: number,
  xAkoyaInteractionType?: XAkoyaInteractionTypeEnum,
  mode?: ModeEnum,
  requestOptions?: RequestOptions
): Promise<ApiResponse<TransactionsEntity>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `string` | Template, Required | Akoya major version number. Do not use minor version numbers. For instance, use v2 and not v2.2 |
| `providerId` | `string` | Template, Required | Id of provider |
| `accountId` | `string` | Template, Required | Account Identifier |
| `startTime` | `string \| undefined` | Query, Optional | ISO 8601 date format in UTC time zone. If blank, the default value (current date - 15 calendar days) is used. If a value is specified, endTime is required. |
| `endTime` | `string \| undefined` | Query, Optional | ISO 8601 date format in UTC time zone. If blank, the default value (current date) is used. If a value is specified, startTime is required. |
| `offset` | `string \| undefined` | Query, Optional | The number of items to skip before the first in the response. The default is 0.<br><br>**Default**: `'0'` |
| `limit` | `number \| undefined` | Query, Optional | The maximum number of items to be returned in the response. The default is 50.<br><br>**Default**: `50` |
| `xAkoyaInteractionType` | [`XAkoyaInteractionTypeEnum \| undefined`](../../doc/models/x-akoya-interaction-type-enum.md) | Header, Optional | Optional but recommended header to include with each data request.<br>Allowed values are `user` or `batch`.<br>`user` indicates a request is prompted by an end-user action.<br>`batch` indicates the request is part of a batch process. |
| `mode` | [`ModeEnum \| undefined`](../../doc/models/mode-enum.md) | Query, Optional | BETA. Default is raw. Use standard for FDX-aligned, standardized data values. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [TransactionsEntity](../../doc/models/transactions-entity.md).

## Example Usage

```ts
const version = 'v2';

const providerId = 'mikomo';

const accountId = ':accountId';

const startTime = '03/30/2020 04:00:00';

const endTime = '03/30/2021 04:00:00';

const offset = '0';

const limit = 50;

const xAkoyaInteractionType = XAkoyaInteractionTypeEnum.Batch;

const mode = ModeEnum.Raw;

try {
  const { result, ...httpResponse } = await transactionsController.getTransactions(
  version,
  providerId,
  accountId,
  startTime,
  endTime,
  offset,
  limit,
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
  "links": {
    "prev": {
      "href": "/transactions/v2/mikomo/33fbd9e5-9cc3-3d7d-15b3-70d97d87ca1d?endTime=2021-02-26T00%3A00%3A00Z&limit=5&offset=0&startTime=2019-02-26T00%3A00%3A00Z"
    }
  },
  "transactions": [
    {
      "depositTransaction": {
        "accountId": "33fbd9e5-9cc3-3d7d-15b3-70d97d87ca1d",
        "amount": 0.29,
        "debitCreditMemo": "CREDIT",
        "description": "Interest Paid This Period",
        "postedTimestamp": "2021-01-27T00:00:00Z",
        "status": "POSTED",
        "transactionId": "22ef95ee-6127-382d-a28c-5b8b7a15d2eb",
        "transactionTimestamp": "2021-01-27T00:00:00Z",
        "transactionType": "INTEREST"
      }
    },
    {
      "depositTransaction": {
        "accountId": "33fbd9e5-9cc3-3d7d-15b3-70d97d87ca1d",
        "amount": 0.13,
        "debitCreditMemo": "CREDIT",
        "description": "Interest Paid This Period",
        "postedTimestamp": "2021-02-24T00:00:00Z",
        "status": "POSTED",
        "transactionId": "f3fced9d-a7a2-4194-5a17-a2a9b09ff64a",
        "transactionTimestamp": "2021-02-24T00:00:00Z",
        "transactionType": "INTEREST"
      }
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`CustomError`](../../doc/models/custom-error.md) |
| 401 | Customer not authorized. | [`CustomError`](../../doc/models/custom-error.md) |
| 404 | 701 - Tax Lots not found. The `holdingId` may be wrong. | [`CustomError`](../../doc/models/custom-error.md) |
| 405 | Method Not Allowed | `ApiError` |
| 406 | Content Type not Supported | [`CustomError`](../../doc/models/custom-error.md) |
| 408 | Request timed out (round trip call took >10 seconds). | [`CustomError`](../../doc/models/custom-error.md) |
| 429 | 1207 - Too many requests | [`CustomError`](../../doc/models/custom-error.md) |
| 500 | Catch-all exception where request was not processed due to an internal outage/issue. | [`CustomError`](../../doc/models/custom-error.md) |
| 501 | FdxVersion in header is not implemented. | [`CustomError`](../../doc/models/custom-error.md) |
| 503 | System is down for maintenance. | [`CustomError`](../../doc/models/custom-error.md) |

