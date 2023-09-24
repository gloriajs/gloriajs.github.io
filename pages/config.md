---
title: Configuration
name: Configuration
description: Information on configuration files for GloriaJS
layout: documentation
category: documentation
permalink: documentation/config
---

## Gloria JS Configuration

`_config.yml`: This file holds the instructions for building your site.

The default configuration looks something like this:

```
include:
    - pages
name: Daveed Silva
tagline: Personal website for Daveed Silva
author: daveed
dest: build
copy:
    - public
exclude:
    - .draft.md
theme:
    - layouts/tailwind
css: tailwind
engine: default
version: '2'
```
