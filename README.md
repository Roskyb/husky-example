# HUSKY EXAMPLE WITH COMMIT LINT FOR WINDOWS



## Install dependencies

```bash
npm install --save-dev @commitlint/config-conventional @commitlint/cli
```
## Create commitlint config
```
touch .commitlintrc.json
```

## Add content to .commitlintrc.json
```json
{
  "extends": ["@commitlint/config-conventional"]
}
```

## Launch husky init
```bash
# It creates a pre-commit script in .husky/ and updates the prepare script in package.json.
npx husky init
```