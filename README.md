# mota-demo

MOTA ĐApp Framework ₡ore (SvelteKit, Core Blockchain, multi-chain).

## Overview

- SvelteKit + MOTA stack
- Addon CLI: `npx addon <repo> <generator> <action>`
- Hidden addon control files supported: `prompt.js`, `_scripts.ejs.sh` / `_scripts.sh`, `_config.ejs.json5` / `_config.json5`
- **i18n** – typesafe-i18n (see [Translations](#translations))
- **Template** – `https://github.com/bchainhub/mota-dapp`
- `.editorconfig`

## Run dev server

```bash
npm install
npm run dev
```

## Addons

Install an addon:

```bash
npx addon <repo> <generator> <action>
```

Examples:

```bash
npx addon bchainhub@mota-addon-support support install
npx addon owner/repo name-of-addon uninstall
npx addon owner/repo name-of-addon install --cache
npx addon owner/repo name-of-addon install --dry-run
```

Addon action folders can contain:

```text
<generator>/<action>/
  prompt.js
  *.ejs.t
  _scripts.ejs.sh
  _scripts.sh
  _config.ejs.json5
  _config.json5
```

- `prompt.js` collects answers once and those values are reused in templates, scripts, and config.
- `*.ejs.t` are normal Hygen templates and are copied/generated into the project.
- `_scripts*` files are rendered/executed automatically and are never copied.
- `_config*` files are rendered/applied automatically and are never copied.
- `_config*` currently targets the `modules` block in `vite.config.ts`.

## Resources

- [📦 MOTA addons search](https://github.com/topics/mota-addon)
- [📖 MOTA skills search](https://skills.sh)

## Translations

i18n is provided by **typesafe-i18n**.

- `npm run i18n:extract` – extract strings from the project
- `npm run i18n:watch` – watch and update translations

## License

CORE. See [LICENSE](LICENSE) in the repo root.
