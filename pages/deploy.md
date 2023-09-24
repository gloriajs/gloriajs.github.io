---
title: Deployment
name: Deployment
description: How to deploy GloriaJS sites with Github Actions
layout: documentation
category: documentation
permalink: documentation/deploy
---

The easiest way to host GloriaJS projects is github files, but you can build the
site with this suggested combination of commands and copy them to any static
hosting provider.

```
yarn run css:tailwind
yarn run copy
```

# Github Pages

Visit your Github Pages settings for the repo and configure it to use Github Actions.
This will allow you to provide a bunch of static files that are uploaded and served as is.

Change your `package.json` to add the following scripts:

```
"scripts": {
  "test": "echo 'tested'",
  "copy": "./node_modules/gloriajs/bin/gloria copy",
  "css:tailwind": "./node_modules/gloriajs/bin/gloria css:tailwind",
  "build": "./node_modules/gloriajs/bin/gloria build"
},
```

Create a `.github/workflows/build_and_deploy.yml` file replicating ours, like:

```
name: Build and Deploy
on:
  push:
    branches:
      - main
permissions:
  contents: write
  pages: write
  id-token: write

jobs:
  build-and-deploy:
    concurrency: ci-${{ github.ref }} # Recommended if you intend to make multiple deployments in quick succession.
    runs-on: ubuntu-latest
    steps:
      - name: Checkout 🛎️
        uses: actions/checkout@v3

      - name: Set up node
        uses: actions/setup-node@v3
        with:
          node-version: 16

      - name: Install
        run: yarn install --ignore-optional

      - name: Build 🔧 # Creates the build folder to deploy
        run: yarn css:tailwind

      - name: Copy 🔧 # Copies public folder to dest
        run: yarn copy

      - name: Upload Artifact
        uses: actions/upload-pages-artifact@v1
        with:
          path: ./build # The folder the action should deploy.
          name: github-pages
          retention-days: 1

      - name:  Deploy  🚀
        uses: actions/deploy-pages@v1
```

This instructions will likely change as commands are added and improved.

# Static web hosting

Similar instructions should work out of the box for any static website provider,
run the `build` or `css:tailwind` commands followed by `copy` to generate the
contents of the build folder and upload those resulting files to your hosting
provider.

# AWS S3

Follow instructions for static website hosting and upload the resulting files to
an S3 bucket configured for
<a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/HostingWebsiteOnS3Setup.html" rel="noopener" target="_blank">
static website providing</a>.
