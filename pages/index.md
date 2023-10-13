---
name: GloriaJS
title: GloriaJS - Home
description: Documentation website for gloria
layout: full
permalink: '/'
---
<header class="relative
        z-10
        pt-[120px]
        px-4
        md:pt-[130px]
        lg:pt-[160px]
        pb-[100px]
        bg-primary
        overflow-hidden">
    <div class="inner">
        <h1>Welcome to {{page.name}}</h1>
        <h2>{{page.description}}</h2>
    </div>
</header>
<div class="container mx-auto px-4">
    <h1>Join Gloria</h1>
    <p>
        <em>gloria is spanish for glory, also the name of my mom and the name was available in npm</em>
    </p>
    <p>We're using github discussions to connect and talk about features, requests and support.
        <a href="https://github.com/gloriajs/gloria/discussions/">Github Discussions</a>.
    </p>
    <p>To install and get started, find us in
        <a href="https://github.com/gloriajs/gloria/">Github</a> and
        <a href="https://www.npmjs.com/package/gloriajs/">NPM</a>.
    </p>
    <h2>Docs</h2>
    <p>
        Checkout the list of available
        <a href="/documentation/commands/">Commands</a> and their respective documentation:
    </p>
    <h2>Install</h2>
    <p>
        <a href="/documentation/install/">Install</a>
        gloria by adding a single npm package to your project and optional configuration files.
    </p>
    <h2>Deploy</h2>
    <p>
        <a href="/documentation/deploy/">Deploy</a>
        your site to github pages, with .actions with a couple changes to your
        <a href="https://github.com/gloriajs/gloriajs.github.io/blob/main/package.json" target="_blank" rel="noopener">
        package.json</a>
        and
        <a href="https://github.com/gloriajs/gloriajs.github.io/blob/main/.github/workflows/build_and_deploy.yml" target="_blank" rel="noopener">
        .github/workflows</a>.
    </p>
    <h2>Examples</h2>
    <p><strong>Some websites built by our friends:</strong></p>
    <p>
    <p>
        <a href="/"><strong>This website</strong></a>:
        <a href="https://github.com/gloriajs/gloria-docs" target="_blank" rel="noopener">Github</a>.
    </p>
    <p>
        <a href="https://caliman.org"target="_blank" rel="noopener"><strong>Kalima corp</strong></a>:
        <a href="https://github.com/calimania/calimania.github.io" target="_blank" rel="noopener">Github</a>.
    </p>
    <p>
        <a href="https://santocabron.com" target="_blank" rel="noopener"><strong>Santo Cabrón</strong></a>:
        <a href="https://github.com/santocabron/santocabron.github.io" target="_blank" rel="noopener">Github</a>
        was built using gloria without access to documentation.
        <br>
        and look at the speed of those builds
        <br>
        <img src="/images/santo-cabron-build-logs.png" alt="Santo Cabrón built times in github" class="max-w-screen-md" style="max-width: 100%;">
    </p>
</div>
