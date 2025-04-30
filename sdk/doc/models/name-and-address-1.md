
# Name and Address 1

Insured name and address

## Structure

`NameAndAddress1`

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
| `name1` | `string \| undefined` | Optional | Name line 1 |
| `name2` | `string \| undefined` | Optional | Name line 2 |

## Example (as JSON)

```json
{
  "line1": "line16",
  "line2": "line28",
  "line3": "line36",
  "city": "city4",
  "region": "region0"
}
```

