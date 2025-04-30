
# Option Security Entity

Information about the option security specific to the type of security

## Structure

`OptionSecurityEntity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `secured` | [`SecuredEnum \| undefined`](../../doc/models/secured-enum.md) | Optional | How the option is secured |
| `optionType` | [`OptionTypeEnum \| undefined`](../../doc/models/option-type-enum.md) | Optional | - |
| `strikePrice` | `number \| undefined` | Optional | Strike price / Unit price |
| `expireDate` | `string \| undefined` | Optional | Expiration date of option |
| `sharesPerContract` | `number \| undefined` | Optional | Shares per contract |

## Example (as JSON)

```json
{
  "secured": "COVERED",
  "optionType": "CALL",
  "strikePrice": 0.6,
  "expireDate": "2016-03-13T12:52:32.123Z",
  "sharesPerContract": 217.4
}
```

