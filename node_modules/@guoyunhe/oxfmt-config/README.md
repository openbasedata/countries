# @guoyunhe/oxfmt-config

![Version](https://img.shields.io/npm/v/@guoyunhe/oxfmt-config)
![Downloads](https://img.shields.io/npm/dw/@guoyunhe/oxfmt-config)

Shared configuration for oxfmt by Guo Yunhe.

## Install

```bash
npm i -D @guoyunhe/oxfmt-config
```

## Example

```ts
// oxfmt.config.ts
import config from '@guoyunhe/oxfmt-config';

export default config;
```

If you want to customize the configuration, you can do it like this:

```ts
// oxfmt.config.ts
import { defineConfig } from 'oxfmt';
import config from '@guoyunhe/oxfmt-config';

export default defineConfig({
  ...config,
  printWidth: 80,
});
```

## License

MPL-2.0
