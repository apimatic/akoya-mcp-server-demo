
# HATEOAS Link

REST application constraint (Hypermedia As The Engine Of Application State)

## Structure

`HATEOASLink`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | URL to invoke the action on the resource |
| `action` | [`ActionEnum \| undefined`](../../doc/models/action-enum.md) | Optional | HTTP Method to use for the request |
| `types` | [`TypeEnum[] \| undefined`](../../doc/models/type-enum.md) | Optional | Content-types that can be used in the Accept header. |

## Example (as JSON)

```json
{
  "href": "https://api.fi.com/fdx/v4/accounts/12345",
  "action": "DELETE",
  "types": [
    "image/gif"
  ]
}
```

