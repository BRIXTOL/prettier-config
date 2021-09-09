## @brixtol/prettier-config

This package includes the shareable Prettier configuration consumed by [Brixtol Textiles](https://www.brixtoltextiles.com).

### Install

[pnpm](https://pnpm.js.org/en/cli/install)

```cli
pnpm add @brixtol/prettier-config --save-dev
```

### Usage

We extend configuration from within `package.json` files.

```json
{
  "prettier": "@brixtol/prettier-config"
}
```

### Ignore JavaScript and TypeScript

Each repository will need to include a `.prettierignore` file that excludes both `.js` and `.ts` files. Prettier wreaks havoc in the development workspace when being used in combination with ESLint and VSCode, so ignore its use on those files.

### Related

- [@brixtol/eslint-config-javascript](https://github.com/brixtol/eslint-config-javascript)
- [@brixtol/eslint-config-typescript](https://github.com/brixtol/eslint-config-typescript)

### License

[MIT](#LICENCE)

---

We [♡](https://www.brixtoltextiles.com/discount/4D3V3L0P3RS]) open source!
