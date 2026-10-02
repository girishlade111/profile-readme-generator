<div align="center">
  <h1>Profile Readme Generator</h1>
  <h3>The best profile readme generator you will find!</h3>
  <p>
    <a href="https://profile-readme-generator.com">Live Demo</a>
  </p>
</div>

Beautify your GitHub profile with this amazing tool — create your profile README your way, simply and fast. This is a fork of [maurodesouza/profile-readme-generator](https://github.com/maurodesouza/profile-readme-generator), maintained by Girish Lade, with multilingual (i18n) support and a modernised Next.js codebase.

## Features

- **Visual section builder** — drag-and-drop canvas to compose your profile README.
- **Rich sections** — text, images, social links, tech badges, GitHub stats, activities, music, borders, alignment and more.
- **Live markdown preview** — see exactly what your profile will look like as you build it.
- **Multi-language UI** — built-in internationalisation via `next-intl`.
- **Copy/export** — one-click copy of the generated markdown, ready to paste into your profile README.
- **State persistence** — your work is saved locally (mobx-persist-store), so you never lose progress.
- **E2E + unit tested** — Playwright end-to-end tests and Vitest unit tests.

## Tech Stack

- **Framework:** Next.js 16 (App Router) + React
- **Styling:** Tailwind CSS
- **State:** MobX / mobx-persist-store
- **i18n:** next-intl
- **Lint/format:** Biome
- **Testing:** Vitest, Playwright
- **Markdown pipeline:** remark / rehype (unified), prismjs syntax highlighting

## Quick Start

### Prerequisites

- Node.js 20+
- npm (or pnpm)

### Install & run

```bash
git clone https://github.com/girishlade111/profile-readme-generator.git
cd profile-readme-generator
npm install --legacy-peer-deps
npm run dev
```

Open http://localhost:3000.

### Build (static export)

```bash
npm run build
```

This produces a static `out/` directory (via `output: 'export'`), deployable to any static host.

### Tests

```bash
npm test            # unit tests (vitest)
npm run test:e2e    # end-to-end tests (playwright)
```

## Project Structure

```
src/
├── app/[locale]/        # App Router pages with locale segment
├── components/          # atoms, molecules, organisms, templates
├── features/            # README section builders (activities, image, music, border, ...)
├── config/              # general + env config
├── i18n/                # next-intl locale setup
├── assets/              # icons, static assets
└── ...
public/                  # static files (manifest, assets)
playwright/              # e2e test fixtures
```

## Environment Variables

No required env vars for the default build. Check `src/config/envs` if you extend the app.

## Deployment

The repo is configured for static export (`output: 'export'` in `next.config.js`). The static site in `out/` is deployed to Cloudflare Pages.

## License

MIT — see [LICENSE.md](./LICENSE.md). Original project by [maurodesouza](https://github.com/maurodesouza); fork maintained by Girish Lade.

---

Built by Girish Lade — https://ladestack.in
