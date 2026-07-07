---

title: Overview
description: Learn what the `generaltranslation` core library does and when to use it directly.

---

# Overview

The `generaltranslation` library is GT's core i18n library for translation, formatting, and locale utilities.

Most framework apps should start with [gt-next](/docs/platform/next/get-started) or [gt-react](/docs/platform/react/get-started). Use `generaltranslation` directly when you want lower-level control, a custom workflow, or translation utilities outside a framework integration.

## What `generaltranslation` does

`generaltranslation` gives you direct access to:

- **String translation** for translating strings or structured content from code.
- **File translation** for uploading source files, queueing translation jobs, checking status, and downloading translated output.
- **Locale utilities** for validating, comparing, resolving, and displaying locale codes.
- **Formatting utilities** for locale-aware numbers, dates, messages, lists, and relative time.



## When to use `generaltranslation`

Use `generaltranslation` when you need to:

- Translate content from a script, backend service, worker, or custom build step.
- Upload and download translation files without using the CLI.
- Build custom translation automation around Project files, jobs, branches, or tags.
- Format numbers, dates, messages, or locale names outside React or Next.js.
- Share GT behavior across packages that do not use the same frontend framework.



## Basic usage

Create a [GT](/docs/platform/core/reference/gt-class/constructor) instance with your Project ID, API key, and default locales, then call [translate](/docs/platform/core/reference/gt-class-methods/translation/translate) to translate a string.

```typescript title="index.ts"
import { GT } from 'generaltranslation';

const gt = new GT({
  apiKey: 'your-api-key',
  projectId: 'your-project-id',
  sourceLocale: 'en',
  targetLocale: 'es',
});

const result = await gt.translate('Hello, world!', 'es');

if (result.success) {
  console.log(result.translation); // "¡Hola, mundo!"
} else {
  console.error(`Translation failed: ${result.error}`);
}
```

Translation methods require an API key and Project ID. Formatting and locale utilities can also be used without translation API access.

## What to read next

- [Quickstart](/docs/platform/core/get-started/quickstart) shows the fastest path to setup and translate your first string.
- [Locales](/docs/platform/core/guides/locales) explains locale codes and supported locales.
- [Translate strings](/docs/platform/core/guides/translate-string) explains how to run runtime string translation.
- [Translate files](/docs/platform/core/guides/translate-file) explains how to upload, queue, status, and download workflows for files.



## Reference sections



### GT class

Use the [GT](/docs/platform/core/reference/gt-class/constructor) class when you want a configured client for translation, formatting, and locale utilities.

- [GT class](/docs/platform/core/reference/gt-class/constructor): Constructor and configuration methods.



### Translation

Use translation methods to translate content, upload files, queue jobs, check status, and download translated files.

- [Translation methods](/docs/platform/core/reference/gt-class-methods/translation/translate): [translate](/docs/platform/core/reference/gt-class-methods/translation/translate), [translateMany](/docs/platform/core/reference/gt-class-methods/translation/translate-many), [uploadSourceFiles](/docs/platform/core/reference/gt-class-methods/translation/upload-source-files), [enqueueFiles](/docs/platform/core/reference/gt-class-methods/translation/enqueue-files), [queryFileData](/docs/platform/core/reference/gt-class-methods/translation/query-file-data), [downloadFile](/docs/platform/core/reference/gt-class-methods/translation/download-file), and related methods.



### Formatting

Use formatting utilities for locale-aware UI output.

- [Formatting methods](/docs/platform/core/reference/gt-class-methods/formatting/format-num): Formatting methods on the [GT](/docs/platform/core/reference/gt-class/constructor) class.
- [Formatting functions](/docs/platform/core/reference/utility-functions/formatting/format-num): Standalone formatting utilities.



### Locales

Use locale utilities to validate, normalize, compare, and display locale codes.

- [Locales](/docs/platform/core/guides/locales): Locale code format, supported locales, and common examples.
- [Locale methods](/docs/platform/core/reference/gt-class-methods/locales/determine-locale): Locale methods on the [GT](/docs/platform/core/reference/gt-class/constructor) class.
- [Locale functions](/docs/platform/core/reference/utility-functions/locales/determine-locale): Standalone locale utilities.



### Types

Use the TypeScript reference when building typed integrations.

- [Types](/docs/platform/core/reference/types/content): Core types for configuration, content, files, entries, variables, and translation results.

