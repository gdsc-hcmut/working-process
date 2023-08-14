# Commitlint, ESLint and Prettier

## Setup Commitlint

1. Firstly, we need to install the commitlint CLI and add a commitlint config
```
npm install @commitlint/cli @commitlint/config-conventional --save-dev
or
yarn add -D @commitlint/cli @commitlint/config-conventional
```
2. We need to add some configuration to a file named `commitlint.config.js`. Sample [here](./templates/commitlint)
3. Now we need to install husky to run commitlint as a pre-commit hook.
```
npm install husky --save-dev
# OR
yarn add -D husky
```
4. We also need to enable the husky hooks:
```
npx husky install
# OR
yarn husky install
```
5. We can add a prepare step which enables the husky hooks upon installation:
```
npm set-script prepare "husky install"
```
6. Now that we are done installing husky, we need to add a pre-commit hook to run commitlint before the code is committed.
```
npx husky add .husky/commit-msg "npx --no -- commitlint --edit $1"
# OR
yarn husky add .husky/commit-msg "yarn commitlint --edit $1"
```

## Setup eslint
1. Install eslint with airbnb
```
npx install-peerdeps --dev eslint-config-airbnb
```
2. Then, add files `.eslintrc`, `.eslintignore` to the root of repo. Use these [sample](./templates/eslint)

3. Install extension **ESLint** and enable it.

## Setup prettier
1. Install Prettier and other related packages to make sure its work does not conflict with ESLint
```
npm install --save-dev prettier eslint-plugin-prettier eslint-config-prettier
```
2. Add [these files](./templates/prettier) to your repo.
3. Install extension **Prettier** and enable it.

## Setup lint-staged
1. Install lint-stage package
```
npm install --save-dev lint-staged
```
2. add file `pre-commit` to **.husky** folder. Sample [here](./templates/lint-staged)
3. add file `.lintstaged.json` to the root of repo. Sample [here](./templates/lint-staged)