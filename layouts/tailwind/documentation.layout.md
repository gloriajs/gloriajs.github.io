---
name: documentation
---
<html lang="en">
    <head>
        <title>{{page.title}} | GloriaJS</title>
        <meta name="description" content="{{page.description}}">
        <link rel="stylesheet" href="/stylesheets/stylesheet.css">
    </head>
    <body>
        <header class="relative
            z-10
            pt-[120px]
            px-4
            md:pt-[130px]
            lg:pt-[160px]
            pb-[100px]
            bg-primary
            overflow-hidden">
                <h1>{{page.name}}</h1>
                <h2>{{page.description}}</h2>
        </header>
        <div class="container mx-auto px-4">
            {{{page.html}}}
        </div>
        <script src="/scripts/gloria.js"></script>
        <script src="/prism/prism.js"></script>
    </body>
</html>
