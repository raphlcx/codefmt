# codefmt

Tired of setting up code linter and formatter every time you start a new project? Or perhaps, you don't want to spend too much time tinkering with these setup?

Then, this guide is for you.

The motivation behind this project is to document the quickest way to setup linter and formatter on your new project.

## Go

On the project root directory, run the following:

```
go fmt ./...
```

## JavaScript

Install ESLint and Prettier:

```
npm install --save-dev --save-exact eslint eslint-config-prettier prettier
```

On the project root directory, create ESLint flat config, `eslint.config.js`, with the following content:

```
import js from "@eslint/js";
import prettier from "eslint-config-prettier";

export default [js.configs.recommended, prettier];
```

Lint with the following command:

```
eslint <dir>
```

Format with the following command:

```
prettier --write <dir>
```

## Python 3

Install Pylint and Black.

```
pip3 install pylint black
```

Lint with the following command:

```
python3 -m pylint <dir>
```

Format with the following command:

```
python3 -m black <dir>
```
