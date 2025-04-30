
# Getting Started with Akoya APIs v2.4.0

## Introduction

Akoya product APIs for data access. Default servers are set for the Akoya sandbox environment.

Akoya APIs include the following updates:

- v2.4.0
  - Added Tax product
- v2.3.0
  - Removed erroneous `accountId` query param from Taxlots endpoint
  - Added TaxLots endpoint
- v2.2.2
  - Added mode query parameter to Account Information, Balances, Investments, and Transactions to support standard mode.
  - Edited callouts for Account Holder endpoint
- v2.2.1
  - Fixed typo in `accountIds` query parameter for `/accounts-info`, `/balances`, `/accounts`
  - Added security method for `Account holder information` to bear token. Missing method defaulted to basic auth.
  - Added examples and descriptions to some schemas
  - Added HTTP status `429` FDX error `1207`.
- v2.2 Additions
  - Added optional `x-akoya-interaction-type` header to all endpoints to specify if a request is part of a batch process
  - Update of tags to organize endpoints by Akoya product
  - `206` response added to `/accounts-info`, `/balances`, `/accounts`
- v2.1 New Statements product and Customers product updated with additional endpoint, `Account holder information`.
- v2.0 Launch of Akoya products: Account Info, Balances, Investments, Transactions, Payments, Customers.

## Building

### Requirements

The SDK relies on **Node.js** and **npm** (to resolve dependencies). It also requires **Typescript version 3.9+**. You can download and install Node.js and [npm](https://www.npmjs.com/) from [the official Node.js website](https://nodejs.org/en/download/).

> **NOTE:** npm is installed by default when Node.js is installed.

### Verify Successful Installation

Run the following commands in the command prompt or shell of your choice to check if Node.js and npm are successfully installed:

* Node.js: `node --version`

* npm: `npm --version`

![Version Check](https://apidocs.io/illustration/typescript?workspaceFolder=AkoyaAPIsV240&step=versionCheck)

### Install Dependencies

- To resolve all dependencies, go to the **SDK root directory** and run the following command with npm:

```bash
npm install
```

- This will install all dependencies in the **node_modules** folder.

![Resolve Dependencies](https://apidocs.io/illustration/typescript?workspaceFolder=AkoyaAPIsV240&workspaceName=akoya-apis-v-2-4-0-lib&step=resolveDependency)

## Installation

The following section explains how to use the generated library in a new project.

### 1. Initialize the Node Project

- Open an IDE/text editor for JavaScript like Visual Studio Code. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

- Click on **File** and select **Open Folder**. Select an empty folder of your project, the folder will become visible in the sidebar on the left.

![Open Folder](https://apidocs.io/illustration/typescript?step=openProject)

- To initialize the Node project, click on **Terminal** and select **New Terminal**. Execute the following command in the terminal:

```bash
npm init --y
```

![Initialize the Node Project](https://apidocs.io/illustration/typescript?step=initializeProject)

### 2. Add Dependencies to the Client Library

- The created project manages its dependencies using its `package.json` file. In order to add a dependency on the *Akoya APIs v2.4.0Lib* client library, double click on the `package.json` file in the bar on the left and add the dependency to the package in it.

![Add AkoyaApisV240Lib Dependency](https://apidocs.io/illustration/typescript?workspaceFolder=AkoyaAPIsV240&workspaceName=akoya-apis-v-2-4-0-lib&step=importDependency)

- To install the package in the project, run the following command in the terminal:

```bash
npm install
```

![Install AkoyaApisV240Lib Dependency](https://apidocs.io/illustration/typescript?step=installDependency)

## Test the SDK

To validate the functionality of this SDK, you can execute all tests located in the `test` directory. This SDK utilizes `Jest` as both the testing framework and test runner.

To run the tests, navigate to the root directory of the SDK and execute the following command:

```bash
npm run test
```

Or you can also run tests with coverage report:

```bash
npm run test:coverage
```

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | `Environment` | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `0` |
| httpClientOptions | [`Partial<HttpClientOptions>`](doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| basicAuthCredentials | [`BasicAuthCredentials`](doc/auth/basic-authentication.md) | The credential object for basicAuth |
| bearerAuthCredentials | [`BearerAuthCredentials`](doc/auth/oauth-2-bearer-token.md) | The credential object for bearerAuth |

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

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| production | **Default** Sandbox server |
| environment2 | Products server |

## Authorization

This API uses the following authentication schemes.

* [`basicAuth (Basic Authentication)`](doc/auth/basic-authentication.md)
* [`bearerAuth (OAuth 2 Bearer token)`](doc/auth/oauth-2-bearer-token.md)

## List of APIs

* [Accountinformation](doc/controllers/accountinformation.md)
* [Balances](doc/controllers/balances.md)
* [Customers](doc/controllers/customers.md)
* [Investments](doc/controllers/investments.md)
* [Payments](doc/controllers/payments.md)
* [Statements](doc/controllers/statements.md)
* [Tax](doc/controllers/tax.md)
* [Transactions](doc/controllers/transactions.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](doc/http-client-options.md)
* [RetryConfiguration](doc/retry-configuration.md)

### HTTP

* [HttpRequest](doc/http-request.md)

### Utilities

* [ApiResponse](doc/api-response.md)
* [ApiError](doc/api-error.md)

