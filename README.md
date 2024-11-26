# Netblink Prettier Config

## Installation

### (Step: 1) Prettier + plugins

```bash
npm install -D prettier prettier-plugin-tailwindcss @shufo/prettier-plugin-blade @prettier/plugin-php
```

### (Step: 2) Prettier Config

See: https://prettier.io/docs/en/configuration.html#sharing-configurations

```bash
npm install --dev git@github.com:NetBlink/nb-prettier.git
```

### (Step: 3) Package.json

Add this config to your project package.json

```json
"scripts": {
    (...)
    "prettier": "npx prettier **/* --write --ignore-path ./.prettierignore --ignore-unknown --list-different",
    "prettier-check": "npx prettier **/* --check --ignore-path ./.prettierignore --ignore-unknown"
},
"prettier": "@netblink/nb-prettier",
```

### (Step: 4) .prettierignore

Copy the base `.prettierignore` to the root of your app, so the prettier script will not change files inside `node_modules` or `vendor`.
You can add more ignore rules according to your project.

## Usage:

#### Format files:

```bash
npm run prettier
```

#### Check if files are formatted properly:

```bash
npm run prettier-check
```

### VsCode

Open User Settings (json) press `ctrl+p` and type `>User Settings (JSON)`, then copy this:

```json
{
    "editor.formatOnSave": true,
    "editor.detectIndentation": false,
    "files.insertFinalNewline": true,
    "prettier.tabWidth": 4,
    "editor.inlineSuggest.enabled": true,
    "[typescript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[vue]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[html]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[scss]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[css]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[php]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[blade]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
}
```
