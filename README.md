# SDA SE Angular Commons

A collection of common Angular libraries, helpers and tools.

## Packages

_So far no packages are defined here - be the first one to [add a package](#add-a-new-package)!_

<!-- ### [@sda-oss/example](./packages/example) -->
<!-- Description about the example package. -->

## Development

This repo is based on [`NRWL nx`][nx-intro] and contains all required dependencies to develop Angular
libraries. If you plan to contribute to this repo, make sure to read the [CONTRIBUTION](./CONTRIBUTING.md)
guidelines.

Use the following command to setup the repository for development:

```console
$ npm install

> sda-angular-commons@0.0.0 postinstall
> ngcc --properties es2015 browser module main

Compiling @angular/compiler/testing : es2015 as esm2015
...

> sda-angular-commons@0.0.0 prepare
> husky install

husky - Git hooks installed

added 2490 packages, and audited 2491 packages in 51s
```

Here are some commands you can use within this repo:

| Command              | Description                              |
| -------------------- | ---------------------------------------- |
| `npm test`           | Execute all tests                        |
| `npm run clean`      | Cleanup setup and reinstall dependencies |
| `npm run build`      | Build all packages                       |
| `npm run build:prod` | Build all packages with production flag  |
| `npm run format`     | Format all package files                 |
| `npm run lint`       | Lint all package files                   |

To see all available scripts, execute `npm run` in the root folder. Also checkout the commands of the
[NX CLI][nx-cli].

### Add a new package

Use the following command to add a new package of type `lib`. It will generate an empty,
[publishable][nx-publishable] Angular library. For more information check the [`nx generate`][nx-cli-generate]
documentation.

```console
$ npm run create:lib

> sda-angular-commons@0.0.0 create:lib
> nx generate @nrwl/angular:library --publishable

✔ What name would you like to use for the library? · example
UPDATE workspace.json
UPDATE nx.json
CREATE packages/example/README.md
CREATE packages/example/ng-package.json
CREATE packages/example/package.json
CREATE packages/example/tsconfig.lib.json
CREATE packages/example/tsconfig.lib.prod.json
CREATE packages/example/tsconfig.spec.json
CREATE packages/example/src/index.ts
CREATE packages/example/src/lib/example.module.ts
CREATE packages/example/tsconfig.json
UPDATE tsconfig.base.json
CREATE packages/example/jest.config.js
CREATE packages/example/src/test-setup.ts
UPDATE jest.config.js
CREATE packages/example/.eslintrc.json
```

[nx-intro]: https://nx.dev/latest/angular/getting-started/intro
[nx-cli]: https://nx.dev/latest/angular/getting-started/nx-cli
[nx-cli-generate]: https://nx.dev/latest/angular/cli/generate
[nx-publishable]: https://nx.dev/latest/angular/structure/buildable-and-publishable-libraries
