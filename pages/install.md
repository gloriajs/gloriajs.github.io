---
title: Installation instructions
name: installing
description: How to add GloriaJS to your projects
layout: documentation
category: documentation
permalink: documentation/install
---

Add GloriaJS by installing the package from npm.

```
npm install gloriajs
```

Add the following scripts to your `package.json`:

```json
    "local-server": "npx -y http-server build",
    "copy": "./node_modules/gloriajs/bin/gloria copy",
    "css:tailwind": "./node_modules/gloriajs/bin/gloria css:tailwind",
    "build": "./node_modules/gloriajs/bin/gloria build"
```

## Local installation

To run gloria locally, for example for development and testing purposes,
clone the repo in the parent folder and add the following to your `package.json`
scripts:

```
    "gloria-local": "../gloria/bin/gloria",
```

And run commands passing arguments with `--` like:

```
npm run gloria-local -- setup
```

## Configuration files



## Folder Structure



## Next steps

- [CSS]
- [Static Files]
- [Data interpolation]
- [Best practices]
- [Deployment] <a href="/documentation/deploy/">Deploy</a> instructions
available in the documentation for Github Pages.
