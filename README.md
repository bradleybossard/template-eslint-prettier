# template-eslint-prettier

Step by step instructions for setting up a eslint/prettier project


## Steps

### Initialize project directory and add dependencies
```
mkdir <project-name>
cd <project-name>
# initialize git repo
git init
# create package.json with default values
npm init --yes        # create package.json with default values
# install dependencies
npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier
# ignore node_modules
echo node_modules > .gitignore
mkdir src
touch src/index.js
```

### Add the following to ./.eslintrc.js
```
module.exports = {
  parserOptions: {
    ecmaVersion: 8
  },
  extends: "plugin:prettier/recommended"
};
```

### Add the following to  ./.prettierrc.js
```
module.exports = {
  singleQuote: true
}
```

### git add and commit
```
git add -A
git commit -m "Initial commit"
```
