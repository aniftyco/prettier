# @aniftyco/prettier

> Standardized code formatting via [Prettier config](https://prettier.io/docs/en/configuration.html) for NiftyCo projects.

## Install

```sh
npm install --save-dev @aniftyco/prettier
```

## Usage

Reference `@aniftyco/prettier` in your `package.json`:

```json
{
  "name": "my-nifty-app",
  "version": "1.2.4",
  "prettier": "@aniftyco/prettier"
}
```

If you don't want to use `package.json`, you can use any of the supported extensions to export a string:

```jsonc
// `.prettierrc.json`
"@aniftyco/prettier"
```

```javascript
// `prettier.config.js` or `.prettierrc.js`
module.exports = '@aniftyco/prettier';
```

## Extending

This configuration is not intended to be changed, but if you have a setup where modification is required, it is possible. Prettier does not offer an "extends" mechanism as you might be familiar from tools such as ESLint.

To extend a configuration you will need to use a `prettier.config.js` or `.prettierrc.js` file that exports an object:

```javascript
module.exports = {
  ...require('@aniftyco/prettier'),
  semi: false,
};
```
