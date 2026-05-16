# Contributing to SasAi

Thank you for contributing to the SasAi Nexus Terminal project. Please follow the guidelines below to keep the codebase consistent and compliant.

## License Headers

Every new `.ts` or `.tsx` source file **must** begin with the following two-line SPDX header:

```ts
// SPDX-License-Identifier: MIT
// Copyright (c) 2026 SasAi
```

This applies to all source files added under `artifacts/`, `packages/`, or anywhere else in the monorepo. The header must be the very first two lines of the file, before any imports or code.

### Example

```ts
// SPDX-License-Identifier: MIT
// Copyright (c) 2026 SasAi

import { useState } from 'react';

export function MyComponent() {
  // ...
}
```

Files that are auto-generated (e.g. by Orval codegen) are exempt — do not add headers to generated files, as they will be overwritten on the next codegen run.

## Code Style

- Use TypeScript for all source files.
- Follow existing formatting conventions in the file you are editing.
- Run `pnpm install` from the repo root before starting work to ensure all dependencies are in place.

## Development Workflow

```bash
pnpm install
pnpm --filter @workspace/api-server run dev
pnpm --filter @workspace/trading-dashboard run dev
```

## Pull Requests

- Keep changes focused — one logical change per PR.
- Ensure the app builds without errors before opening a PR.
