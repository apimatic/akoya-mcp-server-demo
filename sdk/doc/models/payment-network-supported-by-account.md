
# Payment Network Supported by Account

This provides details required to execute a transaction against the account within the payment network

## Structure

`PaymentNetworkSupportedByAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bankId` | `string \| undefined` | Optional | Bank identifier used by the payment network ie. Routing Number |
| `identifier` | `string \| undefined` | Optional | The number used to identify the account within the payment network. If identifierType is ACCOUNT_NUMBER, this is the account number. |
| `identifierType` | `string \| undefined` | Optional | Type of identifier |
| `type` | `string \| undefined` | Optional | Type of payment network |
| `transferIn` | `boolean \| undefined` | Optional | Can transfer funds to the account using this information |
| `transferOut` | `boolean \| undefined` | Optional | Can transfer funds from the account using this information |

## Example (as JSON)

```json
{
  "bankId": "bankId0",
  "identifier": "identifier2",
  "identifierType": "identifierType4",
  "type": "type0",
  "transferIn": false
}
```

