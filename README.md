# Countries Open Base Data

[![npm version](https://img.shields.io/npm/v/%40openbasedata%2Fcountries)](https://www.npmjs.com/package/@openbasedata/countries)
[![npm downloads](https://img.shields.io/npm/dm/%40openbasedata%2Fcountries)](https://www.npmjs.com/package/@openbasedata/countries)

## How To Use

```bash
npm install @openbasedata/countries
```

`data.json` contains country metadata with:

- `name` and `fullName` in English
- `nativeName` and `nativeFullName` in each country's native language

Other localized translations are split into `/translations/<locale>.json` (one language per file) to keep the main dataset smaller.

## Data Structure

```json
[
  {
    "code": "CN",
    "codeAlpha3": "CHN",
    "flag": "🇨🇳",
    "name": "China",
    "fullName": "People's Republic of China",
    "nativeName": "中国",
    "nativeFullName": "中华人民共和国",
    "population": 1413400000,
    "area": 9596961,
    "languages": ["zh"],
    "currency": "CNY"
  }
]
```

| Field            | Type       | Required | Description                                                                           |
| ---------------- | ---------- | -------- | ------------------------------------------------------------------------------------- |
| `code`          | `string`   | Yes      | ISO 3166-1 alpha-2 country/region code (2 uppercase letters), e.g. `CN`.              |
| `codeAlpha3`          | `string`   | Yes      | ISO 3166-1 alpha-3 country/region code (3 uppercase letters), e.g. `CHN`.             |
| `flag`           | `string`   | Yes      | Unicode flag emoji for the country/region, e.g. `🇨🇳`.                                 |
| `name`           | `string`   | Yes      | English short/common country name.                                                    |
| `fullName`       | `string`   | Yes      | English official/formal country name.                                                 |
| `nativeName`     | `string`   | Yes      | Native-language short/common country name.                                            |
| `nativeFullName` | `string`   | Yes      | Native-language official/formal country name.                                         |
| `population`     | `number`   | Yes      | Total population count as an integer.                                                 |
| `area`           | `number`   | Yes      | Total land area in square kilometers (`km²`).                                         |
| `languages`      | `string[]` | Yes      | List of ISO 639-1 language codes commonly used in that country/region, e.g. `["zh"]`. |
| `currency`       | `string`   | Yes      | Primary ISO 4217 currency code used in that country/region, e.g. `CNY`.               |

## Translations

Translations are stored in `/translations`, one file per locale (for example: `/translations/zh-Hans.json`, `/translations/fr.json`). English is stored directly in `data.json`.

Each translation file has this structure:

```json
{
  "CN": {
    "name": "China",
    "fullName": "People's Republic of China"
  }
}
```
