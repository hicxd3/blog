
+++
date = '2025-02-08T12:00:24+03:00'
title = 'NPM Guide'
categories = [ "javascript", "npm" ]
slug = [ "npm_guide" ]
+++

NPM (Node Package Manager) is a tool for managing packages in the Node.js environment. It allows you to install necessary libraries, manage project dependencies, and configure and edit its metadata.

### Downloading Packages

Packages in NPM are bundles of code that can be a library, a utility, or even a full-fledged application.

Developers use pre-made packages to avoid unnecessary work — instead of writing modules from scratch that already exist, they use ready-made solutions.

In Node.js, packages are installed via the NPM manager and are hosted in public repositories.

To install a package with NPM, use the `install` or `i` command:

```js
npm install create-react-app 
// installs React JS
```

If you need several modules, you can list them all at once, instead of entering commands one by one and waiting for each to finish.

```js
npm install react react-dom 
// installs two packages at once
```

### Installing Dependencies

Dependencies in a project are packages required to run and operate the application. They are listed in the `package.json` file under the `dependencies` section and configured with the `npm init` command:

```bash
npm init
```

This command prompts a few questions about the project name, version, author, etc.  
You can skip these safely.

Use the `--yes` flag to skip all prompts:

```bash
npm init --yes
```

After that, a ready `package.json` file will be generated:

```json
{
    "name": "test",
    "version": "1.0.0",
    "main": "index.js",
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "El'ham",
    "License": "MIT",
    "description": ""
}
```

Now let's add dependencies to the `dependencies` section:

```json
"dependencies": {
    "express": "4.17.1",
    "lodash": "4.17.21"
}
```

Save the file and run:

```bash
npm install
```

NPM will create a `package-lock.json` and download all modules into the `node_modules` folder.

### Automatically Add Dependencies

NPM can automatically add dependencies to `package.json` with flags:

- `--save` or `-S` (for older NPM versions) adds to `dependencies`.
- `--save-dev` or `-D` adds to `devDependencies` (used for development only).

Starting from NPM v5, `--save` is not needed anymore.

### Updating Packages

Use `npm update` to update dependencies listed in `package.json`.

Use the caret `^` to allow minor/patch updates but prevent breaking changes:

```json
"dependencies": {
    "express": "^4.17.1",
    "lodash": "^4.17.21"
}
```

This updates to the latest compatible versions based on semantic versioning:

- MAJOR – breaking changes
- MINOR – new features, no breaking changes
- PATCH – bug fixes

Update a specific package:

```bash
npm update react
```

### Install Specific Versions

If an update introduces a bug, install a previous version:

```bash
npm install react@10.1.0
```

### Running NPM Scripts

You can define custom scripts in `package.json`:

```json
"scripts": {
    "prod": "NODE_ENV=production webpack -p --config webpack.conf.js"
}
```

Run it with:

```bash
npm run prod
```

### package.json Overview

```json
"version": "1.0.0" // current version
"description": "Powerful script"
"main": "app/main.js" // entry point
"scripts": { "say-hi": "echo 'Hello Friends!'" }
"dependencies": {
  "express": "^4.17.1",
  "lodash": "^4.17.21"
}
"engines": {
  "node": ">= 5.0.0",
  "npm": ">= 2.5.0"
}
"author": {
  "name": "Cxd3",
  "email": "hi@cxd3.com",
  "url": "https://cxd3.com"
}
"bugs": "https://github.com/cxd3com/package/issues"
"homepage": "https://cxd3.com"
"devDependencies": {
  "autoprefixer": "^7.1.2",
  "babel-core": "^6.22.1"
}
```

### Versioning Symbols in NPM

| Symbol | Meaning |
|--------|---------|
| `^` | Allow minor and patch updates |
| `~` | Allow only patch updates |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater or equal |
| `<=` | Less or equal |
| `=` | Exact version |
| `-` | Range of versions |
| `*` | Any version |
| `x` | Wildcard version (e.g. `1.x.x`) |

### package-lock.json

The package-lock.json file is automatically generated when you install packages via NPM. Most likely, this file already exists in your project folder. Its main purpose is to lock in all dependencies required for third-party packages to work properly.

Let’s look at an example. Suppose I decided to develop a library for handling online payments. To do that, I used several ready-made modules from NPM and built my own solution on top of them.

Sometime later, you discover my library and decide to include it in your own project. Information about it will be recorded in the package.json file, while all the dependencies my library needs to function will be listed in package-lock.json. In simpler terms, package-lock.json stores information about the dependencies of dependencies.

If you peek into the node_modules folder, you'll find not only the packages you manually installed, but also a bunch of others. These appeared automatically because they’re required for the libraries you’re using to work properly. This is made possible thanks to the entries in package-lock.json.