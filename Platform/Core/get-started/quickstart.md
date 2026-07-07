---

title: Quickstart
description: Install the `generaltranslation` core library, initialize the GT class, and translate your first string.

---

# Quickstart

Use this quickstart to install `generaltranslation`, create a [GT](/docs/platform/core/reference/gt-class/constructor) instance, and run your first translation. For a broader introduction, see the [Overview](/docs/platform/core/get-started/overview).

## 1. Install `generaltranslation`

<Tabs items={['npm', 'yarn', 'bun', 'pnpm']}>

`bash yarn add generaltranslation` 

`bash bun add generaltranslation`  `bash pnpm add generaltranslation` 

## 2. Get an API key

Create a `GT_PROJECT_ID` and `GT_API_KEY` in the dashboard.

Open the [API Keys page](https://dash.generaltranslation.com/api-keys), click **Create API Key**, enter a name, and confirm.

```bash
GT_PROJECT_ID=your-project-id
GT_API_KEY=your-api-key
```

General Translation offers high free rate limits for personal Projects, solo developers, and the community.

## 3. Initialize the GT class

Initialize the [GT](/docs/platform/core/reference/gt-class/constructor) class and securely pass your `GT_PROJECT_ID` and `GT_API_KEY`.

```typescript title="src/index.ts"
import { GT } from 'generaltranslation';

const gt = new GT({
  projectId: 'your-project-id',
  apiKey: 'your-api-key',
});
```

You can configure default locales on the [GT](/docs/platform/core/reference/gt-class/constructor) instance. Use default locales when most calls use the same source or target locale. 

```typescript title="src/index.ts"
const gt = new GT({
  projectId: 'your-project-id',
  apiKey: 'your-api-key',
  sourceLocale: 'en',
  targetLocale: 'es',
});
```

See [GT class](/docs/platform/core/reference/gt-class/constructor) for all constructor options.

## 4. Translate your first string

Call the [translate](/docs/platform/core/reference/gt-class-methods/translation/translate) method to translate your first string. Pass the string you want to translate, and the target locale.

```typescript title="src/index.ts"
const result = await gt.translate('Hello, world!', 'es');

if (result.success) {
  console.log(result.translation); // "¡Hola, mundo!"
} else {
  console.error(`Translation failed: ${result.error}`);
}
```

Read about what [locale codes](/docs/platform/core/guides/locales) are or look up a specific locale code in [supported locales](/docs/platform/dashboard/reference/supported-locales).

## Next steps

- See our guide to [Translate files](/docs/platform/core/guides/translate-file)
- See our full guide to [Translate strings](/docs/platform/core/guides/translate-string)

