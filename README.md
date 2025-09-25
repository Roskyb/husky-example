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

## Create hook
Inside .husky create `commit-msg` file and put:
```
npx commitlint --edit "$1"
```

# AUTOMATIC CHANGELOG AND RELEASES
Using release-please you can automate the release, make sure you enable actions to create pull request from Github Actions. Settings > Actions > General > [X] Allow GitHub Actions to create and approve pull requests

Read limitatations at [https://github.com/googleapis/release-please-action](https://github.com/googleapis/release-please-action)