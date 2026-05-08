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
