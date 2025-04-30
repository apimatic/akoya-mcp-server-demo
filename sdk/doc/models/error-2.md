
# Error 2

Present if an error was encountered while retrieving this form

## Structure

`Error2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `number \| undefined` | Optional | Error code defined by FDX API Specification or Data Provider indicating the error situation which has occurred |
| `message` | `string \| undefined` | Optional | End user displayable information which might help the customer diagnose an error |
| `debugMessage` | `string \| undefined` | Optional | Message used to debug the root cause of the error. Contents should not be used in consumer's business logic. Can change at any time and should only be used for consumer to communicate with the data provider about an issue. Provider can include an error GUID in message for their use. |

## Example (as JSON)

```json
{
  "code": 14,
  "message": "message8",
  "debugMessage": "debugMessage8"
}
```

