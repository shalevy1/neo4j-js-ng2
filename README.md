# Neo4jJs (v2)

A Neo4j graph database editor. Explore your **neo4j** graph, create and edit nodes and relationships

[Features and bugs roadmap](https://trello.com/b/NLtaurIH/neo4j-js-https-githubcom-adadgio-neo4j-js-ng2)

Table of Contents
=================

* [Improvements over v1](#improvements-over-v1)
* [Getting started](#getting-started)
  * [Pre-requisites](#pre-requisites)
  * [Quick configuration](#quick-configuration)
* [Running in production](#running-in-production)
* [Running in development](#running-in-development)
* [Known issues](#known-issues)
* [License](#license)

## Improvements over v1

**Bug improvements**

- Settings can now be updated on the fly via the UI.
- Better separated components thanks to Angular2.
- **Much much cleaner code** for developers to build upon.
- Better events handling in graph and database interaction.
- Annoying bugs and annoying features fixed from v1.

**New features**

- Editable relationships types and properties.
- Links/relationships can be created in the create mode.
- Added a plain *cypher query* mode in the main search bar (*@todo will be deprecated*)
- Settings are served from `neo4j.settings.json` and can be changed on the fly (stored in local storage).

![Demo gif 01](https://github.com/adadgio/neo4j-js-ng2/blob/develop/src/assets/tutos/neo4j-js-tuto-01-low.gif)

![Demo gif 02](https://github.com/adadgio/neo4j-js-ng2/blob/develop/src/assets/tutos/neo4j-js-tuto-02-low.gif)

![Demo gif 03](https://github.com/adadgio/neo4j-js-ng2/blob/develop/src/assets/tutos/neo4j-js-tuto-03-low.gif)

## Getting started

- Clone or download the project
- Rename `neo4j.settings.json.dist` into `neo4j.settings.json`.
- Run `ng serve` or `npm start`.

### Pre-requisites

- Neo4j must be installed [Neo4j quick install instructions here](https://www.digitalocean.com/community/tutorials/how-to-install-neo4j-on-an-ubuntu-vps)
- Neo4j Basic Authentication must have been configured (by default)
- Angular2 CLI is required for running with `ng serve` or building into the `dist` folder.

### Quick configuration

- With Angular2: serve project with `ng serve`and navigate to `http://localhost:4200/`
- Without Angular2: create a virtual host on your machine and point it to the `dist` folder
- Copy `src/assets/neo4j.settings.json.dist` to `neo4j.settings.json` and change with your settings
- Change client `authBasic` value to `Basic: <authString>`. Auth string is a base64 encode of neo4j `username:password`

## Running in production

Clone the repository and point an Apache2 or Nginx virtual host to the `./dist` folder (see `./support` files for examples).

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Known issues

- Chrome:  **Compatibility OK** (no known issues)
- In Firefox local storage is not shared between tabs so you might experience settings or debug logs inconsistent views.

## Licence

You do absolutely what you want with that project (MIT Licence).
