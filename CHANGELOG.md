# Changelog

## 1.1.0 - 2026-05-16

### Added

- Added `codeNumeric` to `data.json` for ISO 3166-1 numeric codes (3-digit string values).

### Changed

- Replaced generic Chinese language code `zh` with script-specific values in `data.json`:
  - `zh-Hans` for China (`CN`) and Singapore (`SG`)
  - `zh-Hant` for Hong Kong (`HK`), Macao (`MO`), and Taiwan (`TW`)
- Renamed country code fields for clarity:
  - `code2` -> `code`
  - `code3` -> `codeAlpha3`

## 1.0.0 - 2026-05-16

### Added

- Initial country and region dataset with ISO codes and flags for 247 entries.
- `languages` field for each country entry.
- Native common and official names in the core dataset.
- ISO 4217 `currency` field for each country entry.
- Multi-language country name coverage with broad locale expansion.
- Per-locale translation files under `translations/`.
- Chinese locale aliases and split locale support (`zh-Hans`, `zh-Hant`, and `zh` alias).
- Package metadata, publish file list, and project funding metadata.
- Formatting tooling via `oxfmt` and shared config.

### Changed

- Refactored translation files to key-value format by country code.
- Promoted English and native names into `data.json` and moved localized data to translation files.
- Renamed Chinese translation locale files to standardized names.
- Expanded README with usage instructions and a full data structure table.
- Optimized package metadata (license, author, keywords, files).

### Fixed

- Corrected multiple locale translation issues where common names and official names differed.
- Locale-specific country name fixes across translations including `af`, `am`, `ar`, `az`, `bn`, `bg`, `br`, `be`, `bs`, and `zh` variants.
- Corrected specific data issues such as Japanese name values and Taiwan Traditional Chinese native full name.
- Added missing language keys for all countries.

### Maintenance

- Updated ignore rules for lockfiles and `node_modules`.
