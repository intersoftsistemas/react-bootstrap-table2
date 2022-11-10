## BN fork

![Build Status](https://github.com/Menogus/react-bootstrap-table2/actions/workflows/node.js.yml/badge.svg)

Esta es una bifurcación del repositorio react-bootstrap-table2 de Allen Fang, que es el repositorio para react-bootstrap-table-next en npm. (también bifurcado de https://github.com/Menogus/react-bootstrap-table2, que lo bifurco de https://github.com/BonnierNews/react-bootstrap-table2)

Esta bifurcación se creó simplemente para pruebas, no deberia usarse en produccion...

Los paquetes específicos de este repositorio se pueden usar a través de gitpkg.now.sh: por ejemplo (paquetes del maestro de etiquetas en este repositorio): 

`yarn add https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2?master`

`yarn add https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-editor?master`

`yarn add https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-filter?master`

`yarn add https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-toolkit?master`

`yarn add https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-paginator?master`


O agregando directamente a package.json.
por ejemplo (paquetes la rama master en este repositorio)
```
    "react-bootstrap-table-next": "https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2?master",
    "react-bootstrap-table2-editor": "https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-editor?master",
    "react-bootstrap-table2-filter": "https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-filter?master",
    "react-bootstrap-table2-paginator": "https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-paginator?master",
    "react-bootstrap-table2-toolkit": "https://gitpkg.now.sh/intersoftsistemas/react-bootstrap-table2/packages/react-bootstrap-table2-toolkit?master",
  
```

# release new version of BN Fork
- locally (in new branch, after making changes, and bumping version string in root package.json):
```bash  
yarn test
yarn build
git add .
git commit -m"Bump version"
git push
```
- on Github
- - merge PR
- - create new release with tag matching new version string in root package.json

## react-bootstrap-table2

Rebuild of [react-bootstrap-table](https://github.com/AllenFang/react-bootstrap-table)

> Note that `react-bootstrap-table2`'s npm module name is [**`react-bootstrap-table-next`**](https://www.npmjs.com/package/react-bootstrap-table-next) due to the name being already taken.

`react-bootstrap-table2` separates some functionalities from its core modules to other modules as listed in the following:

- [`react-bootstrap-table-next`](https://www.npmjs.com/package/react-bootstrap-table-next)
- [`react-bootstrap-table2-filter`](https://www.npmjs.com/package/react-bootstrap-table2-filter)
- [`react-bootstrap-table2-editor`](https://www.npmjs.com/package/react-bootstrap-table2-editor)
- [`react-bootstrap-table2-paginator`](https://www.npmjs.com/package/react-bootstrap-table2-paginator)
- [`react-bootstrap-table2-overlay`](https://www.npmjs.com/package/react-bootstrap-table2-overlay)
- [`react-bootstrap-table2-toolkit`](https://www.npmjs.com/package/react-bootstrap-table2-toolkit)

Not only does this reduce the bundle size of your apps but also helps us have a cleaner design to avoid handling too much logic in the kernel module(SRP).

## Migration

If you are coming from the legacy [`react-bootstrap-table`](https://github.com/AllenFang/react-bootstrap-table/), please check out the [migration guide](./docs/migration.md).

## Usage

See [getting started](https://react-bootstrap-table.github.io/react-bootstrap-table2/docs/getting-started.html).

## Online Demo

See `react-bootstrap-table2` [storybook](https://react-bootstrap-table.github.io/react-bootstrap-table2/storybook/index.html).

## Development

Please check the [development guide](./docs/development.md).

## Running storybook example on your local machine

```sh
# Clone the repo
$ git clone https://github.com/react-bootstrap-table/react-bootstrap-table2.git

# change dir to the cloned repo
$ cd react-bootstrap-table2

# Install all dependencies with yarn
$ yarn install

# Start the stroybook server, then go to localhost:6006
$ yarn storybook

```

**Storybook examples: [`packages/react-bootstrap-table2-example/examples`](https://github.com/react-bootstrap-table/react-bootstrap-table2/tree/master/packages/react-bootstrap-table2-example/examples)**
