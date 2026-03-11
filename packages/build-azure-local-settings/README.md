# @shellicar/build-azure-local-settings

> Build plugin that loads Azure `local.settings.json` with Key Vault reference resolution for non-Azure-Functions apps.

## Installation & Quick Start

```sh
npm i --save-dev @shellicar/build-azure-local-settings
```

```sh
pnpm add -D @shellicar/build-azure-local-settings
```

```ts
// tsup.config.ts
import plugin from '@shellicar/build-azure-local-settings/esbuild';
import { defineConfig } from 'tsup';

export default defineConfig({
  esbuildPlugins: [
    plugin({
      mainModule: './src/main.ts',
    }),
  ],
});
```

```ts
// build.ts (esbuild)
import plugin from '@shellicar/build-azure-local-settings/esbuild';

await build({
  bundle: true,
  plugins: [
    plugin({
      mainModule: './src/main.ts',
    }),
  ],
});
```

## Documentation

For full documentation, visit [the GitHub repository](https://github.com/shellicar/build-azure-local-settings).
