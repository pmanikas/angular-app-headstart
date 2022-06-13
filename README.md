# AngularAppHeadstart

This is an Angular model app with useful custom components.

## Table of Content

- [How to scafold the project from scratch](#how-to-scafold-the-project-from-scratch)
  - [Install Angular on current directory](#install-angular-on-current-directory)
  - [Add ESLint to your project](#add-eslint-to-your-project)
  - [Add Stylelint to your project](#add-stylelint-to-your-project)
- [How to clone the project](#how-to-clone-the-project)
- [How to install the project](#how-to-install-the-project-using-npm-or-yarn)
- [How to run the project in development mode](#how-to-run-the-project-in-development-mode-using-npm-or-yarn)

## How to scafold the project from scratch - **IT'S NOT NEEDED IF YOU CLONE THE PROJECT**

### Install **Angular** on current directory

``` bash
npx @angular/cli@13 --directory ./
```

### Add **ESLint** to your project

``` bash
ng add @angular-eslint/schematics
```

### Add **Stylelint** to your project

1. Install [stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint) on your VSCode from scratch

2. You have then to disable your VSCode linting by adding following settings on `.vscode/settings.json` of your project's root folder. (You can exclude the **SCSS** parts if you don't need it)

    ``` json
        {
            "stylelint.enable": true,
            "css.validate": false,
            "scss.validate": false,
            "stylelint.validate": ["scss"]
        }
    ```

3. Install stylelint and basic styleling configuration to your project:

    - For SCSS

        ``` bash
        npm i -D stylelint stylelint-config-standard-scss stylelint-config-prettier-scss
        ```

    - For vanilla CSS

        ``` bash
        npm i -D stylelint stylelint-config-standard stylelint-config-prettier
        ```

4. Add a `.stylelintrc.json` file at the root of your folder

5. Setup your `.stylelintrc.json` file similarly to this (depending on your needs)

    - For SCSS

        ``` json
            {
                "extends": [
                    "stylelint-config-standard-scss",
                    "stylelint-config-prettier-scss"
                ],
                "rules": {
                    "indentation": 4,
                    "string-quotes": "single",
                    "no-duplicate-selectors": true
                }
            }
        ```

    - For Vanilla CSS

        ``` json
            {
                "extends": [
                    "stylelint-config-standard",
                    "stylelint-config-prettier"
                ],
                "rules": {
                    "indentation": 4,
                    "string-quotes": "single",
                    "no-duplicate-selectors": true
                }
            }
        ```

## How to clone the project

Via HTTPS

``` bash
git clone https://github.com/pmanikas/angular-app-headstart.git .
```

Via SSH

``` bash
git@github.com:pmanikas/angular-app-headstart.git .
```

Include the `.` at the end only if you want to clone to current folder

## How to install the project (using npm or yarn)

``` bash
npm i
```

or

``` bash
yarn
```

## How to run the project in development mode (using npm or yarn)

``` bash
npm run start
```

or

``` bash
yarn start
```
