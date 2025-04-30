
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | `Environment` | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](../doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| basicAuthCredentials | [`BasicAuthCredentials`](auth/basic-authentication.md) | The credential object for basicAuth |
| bearerAuthCredentials | [`BearerAuthCredentials`](auth/oauth-2-bearer-token.md) | The credential object for bearerAuth |

The API client can be initialized as follows:

```ts
const client = new Client({
  basicAuthCredentials: {
    username: 'Username',
    password: 'Password'
  },
  bearerAuthCredentials: {
    accessToken: 'AccessToken'
  },
  timeout: 0,
  environment: Environment.Production,
});
```

## Akoya APIs v2.4.0 Client

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

## Controllers

| Name | Description |
|  --- | --- |
| accountInformation | Gets AccountInformationController |
| balances | Gets BalancesController |
| customers | Gets CustomersController |
| investments | Gets InvestmentsController |
| payments | Gets PaymentsController |
| statements | Gets StatementsController |
| tax | Gets TaxController |
| transactions | Gets TransactionsController |

