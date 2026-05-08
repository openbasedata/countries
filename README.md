# Countries Open Base Data

## How To Use

```bash
npm install @openbasedata/countries
```

`name` and `fullName` entries include localized values for `native`, `en` (English), `zh-CN` (Simplified Chinese), `fr` (French), `de` (German), `es` (Spanish), `ja` (Japanese), `ko` (Korean), `hi` (Hindi), `ar` (Arabic), `pt` (Portuguese), `id` (Indonesian), `ru` (Russian), `vi` (Vietnamese), `tr` (Turkish), `it` (Italian), `pl` (Polish), `uk` (Ukrainian), and `nl` (Dutch).

## Data Structure

```json
[
  {
    "code2": "CN",
    "code3": "CHN",
    "flag": "🇨🇳",
    "name": {
      "native": "中国",
      "en": "China",
      "zh-CN": "中国"
    },
    "fullName": {
      "native": "中华人民共和国",
      "en": "People's Republic Of China",
      "zh-CN": "中华人民共和国"
    },
    "population": 1413400000,
    "area": 9596961,
    "languages": ["zh"]
  }
]
```

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `code2` | `string` | Yes | ISO 3166-1 alpha-2 country/region code (2 uppercase letters), e.g. `CN`. |
| `code3` | `string` | Yes | ISO 3166-1 alpha-3 country/region code (3 uppercase letters), e.g. `CHN`. |
| `flag` | `string` | Yes | Unicode flag emoji for the country/region, e.g. `🇨🇳`. |
| `name` | `object` | Yes | Localized short/common country name keyed by locale code. |
| `name.native` | `string` | Yes | Native-language short/common name. |
| `name.<locale>` | `string` | Optional | Translation of short/common name for a locale key like `en`, `fr`, `zh-CN`, `zh-TW`, etc. |
| `fullName` | `object` | Yes | Localized official/formal country name keyed by locale code. |
| `fullName.native` | `string` | Yes | Native-language official/formal name. |
| `fullName.<locale>` | `string` | Optional | Translation of official/formal name for a locale key like `en`, `fr`, `zh-CN`, `zh-TW`, etc. |
| `population` | `number` | Yes | Total population count as an integer. |
| `area` | `number` | Yes | Total land area in square kilometers (`km²`). |
| `languages` | `string[]` | Yes | List of ISO 639-1 language codes commonly used in that country/region, e.g. `["zh"]`. |
