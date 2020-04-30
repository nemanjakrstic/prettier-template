# Prettier Template Project

Get started with Prettier easily.

### 1. Start From the Template

Go to https://github.com/nemanjakrstic/prettier-template and click on "Use this template" button.

### 2. From from Scratch

Copy the Prettier config file:

```bash
$ curl https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierrc -o .prettierrc
```

Copy the Prettier ignore file (optional):

```bash
$ curl https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierignore -o .prettierignore
```

Install dependencies:

```bash
$ npm install -D prettier pretty-quick husky
```

Add NPM commands:

```json
{
    "scripts": {
        "format": "prettier --write './**/*.{js,css,scss,json,html,md}'",
        "format:check": "prettier --check './**/*.{js,css,scss,json,html,md}'"
    },
    "husky": {
        "hooks": {
            "pre-commit": "pretty-quick --staged"
        }
    }
}
```
