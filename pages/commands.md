---
title: Commands
description: "List of available gloria cli commands"
layout: documentation
category: documentation
permalink: documentation/commands
---

# Usage

After installing gloria, several commands are now available for
you to interact with your page, create new content, build
and distribute easier!

You can find information about the commands and options here.

## Available commands

<!-- - [init](#init) -->
<!-- - [new](#new) -->
- [user your local install](#locally)
- [build](#setup)
- [build](#build)
- [build](#copy)
- [build](#css:tailwind)
<!-- - [serve](#serve) -->
<!-- - [migrate](#migrate) -->
- [help](#help)
- [version](#version)

<a name='locally'></a>
## Run Locally

Checkout [installation](/documentation/install) instructions to set up gloria
locally.

<a name='setup'></a>
## Setup

Tries to create a `_config.yml` with the default settings if none exists.

<a name='copy'></a>
## Copy

Copies the contents of the public folder into the build directory overwriting
any files built previously.


<a name='css:tailwind'></a>
## CSS:Tailwind

Builts the HTML files and runs the `tailwind` command. Creates a resulting
`stylesheets/styles.css` with the classes used on the project.

<a name='build'></a>
## Build

Generates all the pages and interpolates data into them.

Builds the site into the desired destination. By default it will use a folder
name 'build' in the root directory of the project, and will create it if doesn't
exists. If it exists it should delete all it's contents before writing to it.

It won't build to a parent folder. The command will fail if _config.yml is
invalid or not present.

It will traverse the folders specified in the `_config.yml` idealling ignoring
the ones that match the exclude property.

Usage:

```bash
gloria build [dest]

Options:
  --help         Show help                                             [boolean]
  --dest         Destination path or folder to build the site, by default it
                 uses 'site'.                                      [default: ""]
  --clear        When different to false, it will not
                 overwrite other files in the dest folder.       [default: true]
  --git          By default it will ignore the .git directory.
                 I don't see a reason why would you include it, but if you want
                 to use --git=true.                             [default: false]
  --save         By default it will save new configuration arguments in the
                 _config file.                                   [default: true]
  --silent, -s   Limit the amount of output to the console.
                                                      [boolean] [default: false]
  -v, --version  Show version number                                   [boolean]
```
<!-- <a name='init'></a>
## Init

It initializes a new gloria website in the destination folder. This is the only
command that is started from an outside directory. Every other command requires
a `_config.yml` to be present in order to execute.

Usage:

```bash
gloria init mysite
```

Initializes a new site, interactively or using the given parameters.
It will create a base configuration file and sample pages using the desired
layout.

Options:

```bash
  --version      Show version number                                   [boolean]
  --help         Show help                                             [boolean]
  --name         Short name to use in the site's configuration, folder name
                                                                   [default: ""]
  --longname     A longer name to use in your site's content       [default: ""]
  --description  Set a description for your site                   [default: ""]
  --location     Folder where your files and site will be at       [default: ""]
  --layout       There are two layouts currently available:
                 Bootstrap, includes bootstrap css files with several themes
                 form bootswatch
                 Default, is basically an empty layout.   [default: "bootstrap"]
  --interactive  Use the interactive prompt to complete the details
                                                                 [default: true]
  --force        If files exists, overwrite them?               [default: false]
 ``` -->

<!-- <a name='new'></a>
## New

Creates new content, with different templates, depending on the type desired.

Usage:
```bash
new [type] [title]
# Examples:
gloria new post hello-world
gloria new --type=page --title='Contact Us' --description='Contact form.'
```

Options:

```bash
  --version      Show version number                                   [boolean]
  --help         Show help                                             [boolean]
  --type         Type of content to create.
                 post|page|layout|partial|sass|css|public are available.
                                                               [default: "post"]
  --title        Title for the page or content.                    [default: ""]
  --name         Name for the file, if none is provided, title will be used.
                                                                   [default: ""]
  --description  Description for the page or content.              [default: ""]
  --category     Category, usually included in posts.              [default: ""]
  --verbose      Supress logs and warnings                       [default: true]
  --folder       Can be used to prepend to the directory where the file is
                 created.                                          [default: ""]
``` -->


<!-- <a name="migrate"></a>
## Migrate

It will try to migrate a site from a jekyll source to be compatible with gloria.

It works for a little, but it requires some manual work, backup your content first or
create a duplicate and run the command over it, this will overwrite your current files.

- permalink in frontmatter should be transformed to url
- the for syntax is super different to #each
- most partials and helpers won't work
- sass files and coffeescript won't work easily, each case has to be addressed separately

Usage:

```bash
gloria migrate [source]

Options:
  --help         Show help                                             [boolean]
  --source       Source platform.                            [default: "jekyll"]
  --exporto      When specified, the folder where the new files will be exported
                                                                [default: false]
  -v, --version  Show version number                                   [boolean]
  --dest                                                       [default: "docs"]
``` -->

<!-- <a name="serve"></a>
## Serve

Serves the site from the last known destination, or from the specific folder given

Usage:

```bash
gloria serve [dest]

Options:
  --help                  Show help                                    [boolean]
  --dest                  Destination path or folder to serve the site from.
                                                               [default: "site"]
  --port                  Port on which to serve the site.     [default: "3300"]
  --suppress-browser, -b  Don't open the browser automatically.
                                                      [boolean] [default: false]
  --watch, -w             Watchs the source files for changes, and re-builds the
                          site.                        [boolean] [default: true]
  --silent, -s            Limit the amount of output to the console.
                                                       [boolean] [default: true]
  -v, --version           Show version number                          [boolean]
``` -->

<a name="help"></a>
## Help

Running `gloria help` will display the most recent list of commands, options and
their description.


<a name="version"></a>
## version

Running `gloria --version` will display the current version of gloria installed
in the project.
