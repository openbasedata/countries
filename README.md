# Countries Open Base Data

## How To Use

```bash
npm install @openbasedata/countries
```

`data.json` contains country metadata with native names only. Localized translations are split into `/translations/<locale>.json` (one language per file) to keep the main dataset smaller.

## Data Structure

```json
[
  {
    "code2": "CN",
    "code3": "CHN",
    "flag": "🇨🇳",
    "name": {
      "native": "中国"
    },
    "fullName": {
      "native": "中华人民共和国"
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
| `fullName` | `object` | Yes | Official/formal country name object. |
| `fullName.native` | `string` | Yes | Native-language official/formal name. |
| `population` | `number` | Yes | Total population count as an integer. |
| `area` | `number` | Yes | Total land area in square kilometers (`km²`). |
| `languages` | `string[]` | Yes | List of ISO 639-1 language codes commonly used in that country/region, e.g. `["zh"]`. |

## Translations

Translations are stored in `/translations`, one file per locale (for example: `/translations/en.json`, `/translations/zh-CN.json`).

Each translation file has this structure:

```json
[
  {
    "code2": "CN",
    "name": "China",
    "fullName": "People's Republic of China"
  }
]
```
