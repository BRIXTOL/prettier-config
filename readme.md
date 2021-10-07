## @brixtol/prettier-config

This package includes the shareable Prettier configuration consumed by [Brixtol Textiles](https://www.brixtoltextiles.com).

### Install

[pnpm](https://pnpm.js.org/en/cli/install)

```cli
pnpm add prettier @brixtol/prettier-config --save-dev
```

> Prettier is an `optionalDependency` so you will need to install it within your project.

### Usage

We extend configuration from within `package.json` files.

```json
{
  "prettier": "@brixtol/prettier-config"
}
```

### Text Editor (VSCode)

Install the [esbenp.prettier-vscode](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) extension from the marketplace. Depending on how your editor is configured, one may require setting global configuration in a user `settings.json` file:

```json
{
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode" // disabled in brixtol packages
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode" // disabled in brixtol packages
  }
}
```

##### Pnpm monorepo

If you are working within a pnpm monorepo workspace there are 2 ways you can leverage prettier. For us here at [brixtol](https://github.com/brixtol) we provide prettier and the shareable config in the root as developement dependency. You may wish to refer a certain workspace (package) to the shareable config within `.vscode/settings.json` file:

```json
{
  "prettier.configPath": "node_modules/@brixtol/prettier-config/index.js"
}
```

### Ignored Files

We do not leverage prettier for various file types because it is extremely opionated and conflicts with our code styles, especially that found in JavaScript and TypeScript based projects. In almost all packages within our monorepo a `.prettierignore` file is included to prevent prettier from wreaking utter havoc in our development workspace. Below is standard ignores we assert:

```
*.toml
*.mjs
*.js
*.ts
*.css
*.scss
*.liquid
*.html
```

### Related

- [@brixtol/eslint-config](https://github.com/brixtol/eslint-config)
- [@brixtol/browserslist-config](https://github.com/brixtol/browserslist-config)

### License

[MIT](#LICENCE)

---

We [♡](https://www.brixtoltextiles.com/discount/4D3V3L0P3RS]) open source!
