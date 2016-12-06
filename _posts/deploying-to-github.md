---
title: Deploying to Github
description: ""
type: post
layout: ""
category: docs
url: deploying-to-github
---

Gloria is compatible with the new github pages out of the box. Is the easiest
way to deploy your site for free! with support for custom domains and 

[Find more information about Github Pages](https://pages.github.com/)

## Steps

### Build

Build the project to a folder named `docs`.

```bash
gloria build docs
```

### Push

Do git add, commit and push to send your data to github.

Push your project to github, you can use any branch, but master is usually
the best one to use.

### Select the pages source

In the repo settings, there's an option called github pages. The source appears
as `none` by default. If you pushed a `docs` folder there should be an option
that allows you to choose branch master and docs folder.

Github will serve the files from that folder, the same way that `gloria serve` works. 

### ? 

???

### Profit

Share the URL with everyone!

### Additional Steps

#### SSL

CloudFlare and github pages work very well for free SSL,
configure your domain to use the cloudflare DNS and activate the SSL.
You can get more 
[details in their website](https://blog.cloudflare.com/secure-and-fast-github-pages-with-cloudflare/). 

#### Custom domain

Using a custom domain with github pages is super easy!

Change your DNS settings to the following, depending on whether you're using a naked domain or www.

For Apex or naked domain, create two A records pointing to:

```
192.30.252.153
192.30.252.154
```

To use a subdomain, like www, create a CNAME record pointing to:

```
YOUR-GITHUB-USERNAME.github.io
```

[Find more info in their website](https://help.github.com/articles/using-a-custom-domain-with-github-pages/).