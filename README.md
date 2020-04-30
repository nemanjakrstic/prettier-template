# Prettier Template Project

## Why?

Please, watch this great introduction video from the creator of Prettier (8 minutes long):

[![A Prettier Printer by James Long on React Conf 2017](https://prettier.io/docs/assets/youtube-cover/a-prettier-printer-by-james-long-on-react-conf-2017.png)](https://www.youtube.com/watch?v=hkfBvpEfWdA)

## Requirements

Node.js v10 or newer.

## Getting Started

There are two options:

### 1. Use this Template

If you are creating a new project, easiest way to get started is to use this template. Go to https://github.com/nemanjakrstic/prettier-template and click on the "Use this template" button.

### 2. Start from Scratch

First, install the required dependencies:

```bash
$ npm install prettier pretty-quick husky --save-dev
```

Next, add this to your `package.json` file:

`package.json`

```json
{
    "scripts": {
        "format": "prettier --write .",
        "format:check": "prettier --check ."
    },
    "husky": {
        "hooks": {
            "pre-commit": "pretty-quick --staged"
        }
    }
}
```

Create a Prettier config file in the root of the project:

`.prettierrc`

```json
{
    "semi": true,
    "printWidth": 120,
    "trailingComma": "all",
    "singleQuote": true,
    "tabWidth": 4,
    "arrowParens": "avoid"
}
```

Since we want to format all supported files in the project, except the package-lock.json file, we need to create a Prettier ignore file in the root of the project:

`.prettierignore`

```
package-lock.json
```

## Usage

You probably don't need to run the following commands since all changed files will be formatted automatically after you create a commit.

To format all the files manually:

```bash
$ npm run format
```

Check if all files are formatted properly:

```bash
$ npm run format:check
```

### Auto-format on commit

It's strongly recommended to setup your editor to run the Prettier on every file save to take all the advantages that Prettier offers.

Check out the official docs on how to setup your editor integration: https://prettier.io/docs/en/editors.html

## More Info

For more information, check out the official website: https://prettier.io
