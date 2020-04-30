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

First, install the Prettier:

```bash
$ npm install prettier --save-dev
```

Next, add these scripts to your `package.json` file:

`package.json`

```json
{
    "scripts": {
        "format": "prettier --write .",
        "format:check": "prettier --check ."
    }
}
```

Copy the Prettier config file in the root of your project:

You can [download](https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierrc) the file directly or use the command line:

```bash
$ curl https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierrc -o .prettierrc
```

Since we want to format all supported files in the project, except the package-lock.json file, we need to create a Prettier ignore file in the root of the project:

You can [download](https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierignore) the file directly or use the command line:

```bash
$ curl https://raw.githubusercontent.com/nemanjakrstic/prettier-template/master/.prettierignore -o .prettierignore
```

## Usage

To format all the files manually:

```bash
$ npm run format
```

Check if all files are formatted properly:

```bash
$ npm run format:check
```

### Auto-format on Save

It's strongly recommended to setup your editor to run the Prettier on every file save to take all the advantages that Prettier offers.

Check out the official docs on how to setup your editor integration: https://prettier.io/docs/en/editors.html

## More Info

For more information, check out the official website: https://prettier.io
