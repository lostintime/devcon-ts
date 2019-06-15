# DEVCON-TS

[![Travis](https://img.shields.io/travis/lostintime/devcon-ts.svg)](https://travis-ci.org/lostintime/devcon-ts)

Opinionated development configs for TypeScript projects.

Package brings `devDependencies` required for [prettier](https://prettier.io/), [tslint](https://github.com/palantir/tslint#readme) and [conventional commits](https://www.conventionalcommits.org/) support.

## Installation

Install the package and link config files.

```
npm install --save-dev @lostintime/devcon-ts
```

### Conventional Commits

Dependencies brought by `@lostintime/devcon-ts`.

```
ln -s ./node_modules/@lostintime/devcon-ts/.huskyrc
ln -s ./node_modules/@lostintime/devcon-ts/.czrc
ln -s ./node_modules/@lostintime/devcon-ts/.lintstagedrc
ln -s ./node_modules/@lostintime/devcon-ts/.commitlintrc.json
```

### Prettier

```
ln -s ./node_modules/@lostintime/devcon-ts/.editorconfig
ln -s ./node_modules/@lostintime/devcon-ts/.prettierrc
```

### TypeScript

```
ln -s ./node_modules/@lostintime/devcon-ts/tslint.json
```

Extend `@lostintime/devcon-ts` in your `tsconfig.json`, ex:

```json
{
  "extends": "@lostintime/devcon-ts",
  "compilerOptions": {
    "rootDir": "./src",
    "outDir": "./dist",
    "declarationDir": "./dist",
    "composite": true
  },
  "include": ["src"]
}
```

### Testing

... with mocha, chai and nyc.

```
npm install --save-dev mocha chai @types/mocha @types/chai nyc
```

Link configs

```
ln -s ./node_modules/@lostintime/devcon-ts/.mocharc.json
ln -s ./node_modules/@lostintime/devcon-ts/.nycrc
```

### Updates

`mocha.opts` is not deprecated in favor of `.mocharc.json`
