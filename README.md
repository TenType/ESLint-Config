# ESLint Config

[ESLint](https://eslint.org/) is a powerful tool to help developers produce cleaner, more consistent code.
<br>Below are the steps to install ESLint for your code editor in JavaScript and TypeScript with my personal configurations!

## JavaScript Installation
1. Run [`npm install eslint --save-dev`](https://www.npmjs.com/package/eslint) if you don't have ESLint installed on your editor already.
	- If you are using [Visual Studio Code](https://code.visualstudio.com/), you can also install the [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) from the Marketplace to integrate warnings and errors directly in the editor (highly recommended).

2. If you don't want the regular ESLint parser to error on newer versions of ECMAScript, `npm install` the Babel dependencies as well:
<pre>
npm install <a href="https://www.npmjs.com/package/@babel/core">@babel/core</a> <a href="https://www.npmjs.com/package/@babel/eslint-parser">@babel/eslint-parser</a> <a href="https://www.npmjs.com/package/@babel/preset-env">@babel/preset-env</a> --save-dev
</pre>

3. Create a `.babelrc` file:
```json
{
  "presets": [
    ["@babel/preset-env", { "shippedProposals": true }]
  ]
}
```

4. Lastly, create a `.eslintrc.json` file with the [JS configurations](javascript/.eslintrc.json) located in this repository.
	- The configuration in this repository uses the Babel parser, but if you did not install any Babel dependencies from step 2, make sure to remove the parser option in the config file.

5. **Done!** ESLint should be up and running with JavaScript!

## TypeScript Installation
> :warning: **The TypeScript configurations are a work in progress, please check back later for updates.**
1. Run [`npm install eslint --save-dev`](https://www.npmjs.com/package/eslint) if you don't have ESLint installed on your editor already.
	- If you are using [Visual Studio Code](https://code.visualstudio.com/), you can also install the [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) from the Marketplace to integrate warnings and errors directly in the editor (highly recommended).

2. `npm install` the typescript-eslint dependencies:
<pre>
npm install <a href="https://www.npmjs.com/package/@typescript-eslint/eslint-plugin">@typescript-eslint/eslint-plugin</a> <a href="https://www.npmjs.com/package/@typescript-eslint/parser">@typescript-eslint/parser</a> --save-dev
</pre>

3. Create a `.eslintrc.json` file with the [TS configurations](typescript/.eslintrc.json) located in this repository.
	- Make sure you also have [TypeScript](https://www.npmjs.com/package/typescript) installed for the parser to work correctly.

4. **Done!** ESLint should be up and running with TypeScript!
