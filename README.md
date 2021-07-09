# Wonderflow Eslint Configuration [<img src="https://svgshare.com/i/Ygj.svg" alt="Wonderflow Logo" width="90" height="90" align="right">](https://design.wonderflow.ai)

[![Release](https://github.com/wonderflow-bv/eslint-config-wonderflow/actions/workflows/release.yml/badge.svg?branch=main)](https://github.com/wonderflow-bv/eslint-config-wonderflow/actions/workflows/release.yml)

This repository contains the source code of Wonderflow eslint rules to ensure your JS is compliant with Wonderflow JS coding standards.

```sh
npm i @wonderflow/eslint-config
```

## Usage

Extends the configuration from your local `eslintrc` configuration file:

```json
{
  "extends": "@wonderflow/eslint-config"
}
```

### Typescript

To add eslint typescript support you can extend the configuration by adding [the parser and the plugin](https://www.npmjs.com/package/@typescript-eslint/eslint-plugin).

```sh
npm i -D typescript @typescript-eslint/parser @typescript-eslint/eslint-plugin
```

```json
{
  "extends": "@wonderflow/eslint-config",
  "parser": "@typescript-eslint/parser",
  "plugins": ["@typescript-eslint"]
}
```

Then create a `tsconfig.eslint.json` at the project root that extends your typescript configuration:

```json
{
  "extends": "./tsconfig.json"
}
```
