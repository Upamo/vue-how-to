# vue-how-to

## How to setup Prettier with ESLint

### Install Packages

```
npm install \
  eslint \
  babel-eslint \
  eslint-plugin-vue \
  eslint-config-prettier \
  eslint-plugin-prettier \
  @vue/eslint-config-prettier
```

Some of the packages (especially from the top) may also have been installed by Vue CLI.

### Set up ESLint Configuration

The `extends` section in `.eslintrc.js` must look like:

```
  extends: [
    'plugin:vue/essential',
    'plugin:prettier/recommended',
    'eslint:recommended',
    '@vue/prettier'
  ],
```

If there is no own configuration file for ESLint this configuration must be placed in `package.json` under section `eslintConfig` like this:

```
{
  ...
  "eslintConfig": {
    "extends": [
      "plugin:vue/essential",
      "plugin:prettier/recommended",
      "eslint:recommended",
      "@vue/prettier"
    ]
  },
  ...
}
```
