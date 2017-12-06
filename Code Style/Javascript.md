# Javascript

For Javascript projects we will aim to adhere as closely as possible to the [AirBnB Javascript style Guide](https://github.com/airbnb/javascript).

# React

For react projects, all of the above applies, with the addition of the rules from the [AirBnB React style guide](https://github.com/airbnb/javascript/tree/master/react). 

# Development Environment Setup

Each developer should configure their programming environment as follows:

## EditorConfig
 
Code editors should be configured to respect the formatting rules defined by the [Editor Config](http://editorconfig.org/) file included in the git repository. Instructions for your editor can be found [here](http://editorconfig.org/#download).

## ESLint

A code editor set up to perform live validation of [ESLint](https://eslint.org/) rules will result in less incorrect code being checked into git. You can find a list of plugins for common editors [here](https://eslint.org/docs/user-guide/integrations).
Try not to commit files to git which have eslint errors or warnings.

## Auto Fixing

Eslint can automatically fix many types of issues. Running `npm run fix [filename]` should do this if the project has been configured properly.
This is especially useful for fixing incorrect formatting before commiting.

Optionally, it is possible to configure your editor to run this every time you save.

[Atom](https://atom.io/packages/linter-eslint)
[Vim](https://github.com/w0rp/ale)
and 
[Sublime](https://github.com/TheSavior/ESLint-Formatter)
all have plugins. For other editors googling `eslint fix <editorname>` will probably find something.

We might want to look into [Prettier](https://prettier.io/) for this in the future?

# Setting up JS Projects

## Editor Config

Each project will have the [Editor Config](http://editorconfig.org/) provided by AirBnB included in the root folder of the Javascript web UI. This file can be found [here](https://github.com/airbnb/javascript/blob/master/.editorconfig)

## Eslint Rules

The AirBnB style guide has been encoded into a set of eslint rules. These can be easily imported into a project using the npm package [eslint-config-airbnb](https://www.npmjs.com/package/eslint-config-airbnb).

Install the package.
`npm install --save-dev eslint-config-airbnb`.

Add an `.eslintrc` file if one does not exist. The following setup will work for most projects: 
```
{
  "env": {
    "browser": true
  },

  "extends": [
    "airbnb"
  ],

  "rules": {
    "no-console": 0,
    "no-alert": 0
  }
}
```

Add npm scripts to `package.json` to run the linter.
```
"scripts": {
  "lint": "eslint --ext .js --ext .jsx ./src",
  "fix": "eslint --ext .js --ext .jsx --fix ./src"
}
```

Make sure eslint is run as part of a CI build. An easy way to do this is to ad a pre step to whatever npm script runs the build. For example, if you use `npm run dist` to build for production, add a `predist` script which will automatically run eslint first
``` 
"scripts": {
  "predist": "npm run lint"`
}
```
