---
title: Commands
description: ""
type: page
layout: ""
category: documentation
url: documentation/commands
---

After installing gloria, several commands are now available for
you to interact with your page, create new content, build
and distribute easier! 

You can find information about the commands and options here.

## Available commands

- [init](#init)
- [new](#new)
- [build](#build)
- [serve](#serve)
- [migrate](#migrate)
- [help](#help)
- [version](#version)

<a name='init'></a>
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
 ```

<a name='new'></a>
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
```

<a name='build'></a>
## Build

Generates all the pages and posts, copies the assets to the desired location, and
prepares the website to be launched.

Builds the site into the desired destination. By default it will use a folder name 'site' in the root
directory of the project, and will create it if doesn't exists. If it exists it will delete
all it's contents before writing to it.

It won't build to a parent folder. The command will fail if _config.yml is invalid or not present. 

By default it will ignore the .git directory and other files that it considers unnecesary.

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

<a name="serve"></a>
## serve

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
```