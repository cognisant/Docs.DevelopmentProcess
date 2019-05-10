# JavaScript Code Style

For JavaScript projects we will aim to adhere as closely as possible to the [AirBnB JavaScript style Guide](https://github.com/airbnb/javascript), with the addition of [Prettier](https://prettier.io/) to enforce a consistent formatting.

## React

For [React](https://reactjs.org) projects, all of the above applies, with the addition of the rules from the [AirBnB React style guide](https://github.com/airbnb/javascript/tree/master/react).

## Development Environment Setup

Each developer should configure their programming environment as follows:

### EditorConfig

Code editors should be configured to respect the formatting rules defined by the [Editor Config](http://editorconfig.org/) file included in the git repository. Instructions for your editor can be found [here](http://editorconfig.org/#download).

### ESLint

A code editor set up to perform live validation of [ESLint](https://eslint.org/) rules will result in less incorrect code being checked into git. You can find a list of plugins for common editors [here](https://eslint.org/docs/user-guide/integrations).

Files which have ESLint errors or warnings should not be committed to git.

### Prettier

A code editor set up with [Prettier](https://prettier.io/) to auto-format code before saving would result in less badly formatted code being checked into git. Information on editor integration can be found [here](https://prettier.io/docs/en/editors.html).

Files should not be committed to git unless they have had Prettier run against them first.

#### Auto Fixing

ESLint can automatically fix many types of issues. Running `npm run fix` should do this for all files in the project if it has been configured properly.

Running Prettier with the `--write` parameter will automatically format code. Running `npm run format` should do this for all files in the project if it has been configured properly.

These tools are especially useful for fixing incorrect formatting before committing.

It is desirable that your editor is set up to do this automatically on save, instructions for this vary depending on editor and searching for "auto format on save <editor name>" should find the correct instructions, and work as long as the correct plugins are installed for your editor of choice.

## Setting up JS Projects

### Editor Config

Each project will have the below `.editorconfig` file included in the root folder of the JavaScript web UI. It is based on the file provided by AirBnB [here](https://github.com/airbnb/javascript/blob/master/.editorconfig).

```
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
end_of_line = lf
# editorconfig-tools is unable to ignore longs strings or urls
max_line_length = 100
```

### AirBnB ESLint Rules

The AirBnB style guide has been encoded into a set of ESLint rules. These can be easily imported and configured in a project using [eslint-config-airbnb](https://www.npmjs.com/package/eslint-config-airbnb).

### ESLint and Prettier Set Up

With a default installation of both Prettier, and the AirBnB ESLint rules, there will be conflicting rules which will cause issues if these are being enforced during build.

Details on how to set up a project which will use both the ESLint AirBnB Rules, and format the code using Prettier can be found [here](https://blog.echobind.com/integrating-prettier-eslint-airbnb-style-guide-in-vscode-47f07b5d7d6a). The instructions from this article have been provided below with tweaks to match our usage.

1. Install the ESLint and Prettier libraries into our project. In your project’s root directory, you will want to run: `npm install -D eslint prettier`.
2. Install the Airbnb config. If you’re using npm 5+, you can run this shortcut to install the config and all of its dependencies: `npx install-peerdeps --dev eslint-config-airbnb`
3. Install `eslint-config-prettier` (disables formatting for ESLint) and `eslint-plugin-prettier` (allows ESLint to show formatting errors as we type) `npm install -D eslint-config-prettier eslint-plugin-prettier`
4. Create .eslintrc.json file in your project’s root directory:

```
{
  "extends": ["airbnb", "prettier"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": ["error"]
  },
  "env": {
    "browser": true
  },
}
```

A `.prettierrc` file should not be needed as prettier will use the rules specified in the `.editorconfig` file.

### .gitattributes file

To ensure that Windows build agents are able to properly checkout the repository, and maintain the required line endings as specified in the `.editorconfig` file, it is necessary to configure git to not convert `LF` to `CRLF` on checkout. It is possible to do this globally on a build server, but this can be avoided by adding a `.gitattributes` file in the same folder as the `.editorconfig` file with the following content.

```
* text=auto eol=lf
```

### Running ESLint and Prettier

There are many ways of running ESLint and Prettier against the code outside of an editor.

#### npm Scripts

Add npm scripts to `package.json` to run ESLint. Thanks to `eslint-plugin-prettier` we can check all of our style rules simply using ESLint.

```
"scripts": {
  "lint": "eslint --ext .js --ext .jsx ./src",
  "fix": "eslint --ext .js --ext .jsx --fix ./src",
  "format": "prettier --write \"./**/*.{js,jsx}\""
}
```

Make sure ESLint is run as part of a CI build. An easy way to do this is to add a pre-step to whatever npm script runs the build. For example, if you use `npm run dist` to build for production, add a `predist` script which will automatically run ESLint first.

```
"scripts": {
  "predist": "npm run lint"
}
```

#### webpack

If [webpack](https://webpack.js.org) is being used to build the web project, the plugin `eslint-loader` can be utilized to run ESLint against the files without having to also use an npm script. It should be installed using `npm install -D eslint-loader`, then the following rule should be added to the webpack config to use the plugin.

```
rules: [
  {
    test: /\.(js|jsx)$/,
    exclude: /node_modules/,
    use: ['eslint-loader']
  }
]
```

#### Pre-commit Hook

To try and avoid incorrectly formatted code from being committed to a repository, a pre-commit hook should be used to run both Prettier to reformat the code, and ESLint, prior to code being committed to the repository to ensure no linting issues remain.

There is no way of enforcing a pre-commit hook for all users of a repository so the next best thing is to use a tool called [husky](https://github.com/typicode/husky), along with [lint-staged](https://github.com/okonet/lint-staged) which will install pre-commit hooks to run ESLint and Prettier when `npm install` is run in the repository.

The easiest way to set this up is to have both ESLint and Prettier set up, as above, then run `npx mrm lint-staged`, this will install and configure both husky and lint-staged to run the linters using a pre-commit hook based on installed packages and the `lint` and `format` npm scripts above.
