# Payments

Payments

```ts
const paymentsController = new PaymentsController(client);
```

## Class Name

`PaymentsController`


# Payment-Networks

This product supports use cases such as payment enablement or account opening. The response includes identifiers necessary to make ACH and RTP payments. Identifiers include account number, routing number, identifier type (actual or tokenized account number), and payment network type such as ACH or RTP.

<br>
To see the response schema, select the `200` response below. For an example payload response, see the `200` example response below the *Try it* feature.

> 🛑
> 
> The *id_token* should be used as the bearer token with this call.

```ts
async paymentNetworks(
  version: string,
  providerId: string,
  accountId: string,
  xAkoyaInteractionType?: XAkoyaInteractionTypeEnum,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ArrayOfAccountPaymentNetworks>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `string` | Template, Required | Akoya major version number. Do not use minor version numbers. For instance, use v2 and not v2.2 |
| `providerId` | `string` | Template, Required | Id of provider |
| `accountId` | `string` | Template, Required | Account Identifier |
| `xAkoyaInteractionType` | [`XAkoyaInteractionTypeEnum \| undefined`](../../doc/models/x-akoya-interaction-type-enum.md) | Header, Optional | Optional but recommended header to include with each data request.<br>Allowed values are `user` or `batch`.<br>`user` indicates a request is prompted by an end-user action.<br>`batch` indicates the request is part of a batch process. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [ArrayOfAccountPaymentNetworks](../../doc/models/array-of-account-payment-networks.md).

## Example Usage

```ts
const version = 'v2';

const providerId = 'mikomo';

const accountId = ':accountId';

const xAkoyaInteractionType = XAkoyaInteractionTypeEnum.Batch;

try {
  const { result, ...httpResponse } = await paymentsController.paymentNetworks(
  version,
  providerId,
  accountId,
  xAkoyaInteractionType
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
  "paymentNetworks": [
    {
      "bankId": "125000024",
      "identifier": "454992210071",
      "identifierType": "ACCOUNT_NUMBER",
      "type": "US_ACH",
      "transferIn": true,
      "transferOut": true
    }
  ]
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | 602 - Customer does not have authorization to perform this action. The customer may have revoked access through the provider and would need to reauthenticate. | [`CustomError`](../../doc/models/custom-error.md) |
| 403 | 403 - The `providerId` is wrong or your app doesn't have a subscription to the provider. | [`CustomError`](../../doc/models/custom-error.md) |
| 404 | 701 - Account not found. The `accountId` may be wrong. | [`CustomError`](../../doc/models/custom-error.md) |
| 405 | Method Not Allowed | `ApiError` |
| 408 | Request timed out (round trip call took >10 seconds). | [`CustomError`](../../doc/models/custom-error.md) |

