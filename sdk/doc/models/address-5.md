
# Address 5

Box 8, Address of property securing mortgage

## Structure

`Address5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `line1` | `string \| undefined` | Optional | Address line 1 |
| `line2` | `string \| undefined` | Optional | Address line 2 |
| `line3` | `string \| undefined` | Optional | Address line 3 |
| `city` | `string \| undefined` | Optional | City |
| `region` | `string \| undefined` | Optional | State, Province, Territory, Canton or Prefecture. From [Universal Postal Union](https://www.upu.int/en/Postal-Solutions/Programmes-Services/Addressing-Solutions#addressing-s42-standard) as of 2-26-2020, [S42 International Address Standards](https://www.upu.int/UPU/media/upu/documents/PostCode/S42_International-Addressing-Standards.pdf). For U.S. addresses can be 2-character code from '#/components/schemas/StateCode' |
| `postalCode` | `string \| undefined` | Optional | Postal code<br><br>**Constraints**: *Maximum Length*: `16` |
| `country` | [`ISO3166CountryCode2Enum \| undefined`](../../doc/models/iso3166-country-code-2-enum.md) | Optional | Country code |

## Example (as JSON)

```json
{
  "line1": "line12",
  "line2": "line24",
  "line3": "line32",
  "city": "city0",
  "region": "region6"
}
```

