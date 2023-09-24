---
title: Static files
name: Static files
description: How to include images and other static files
layout: documentation
category: documentation
permalink: documentation/static
---


Use the `copy` command to bring over static files.

```
npm run gloria -- copy
```

By default all the files in the `public` folder are copied over to `build`.

Static files will override any pages or other files from the process, this so is
easier to debug, change the name of the file or permalink of the page to prevent
it.
