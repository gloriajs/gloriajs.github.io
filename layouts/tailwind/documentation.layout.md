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
        <nav class="bg-white border-gray-200 dark:bg-gray-900" style="position: absolute; top: 0;">
            <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
                <a href="/" class="flex items-center">
                    <img src="/images/gloria-js.png" class="h-8 mr-3" alt="Gloria JS Logo" />
                </a>
            </div>
        </nav>
        <header class="relative
            z-10
            pt-[120px]
            px-4
            md:pt-[130px]
            lg:pt-[160px]
            pb-[100px]
            bg-primary
            overflow-hidden">
                <div class="inner" style="padding-left: 120px;">
                    <h1>{{page.name}}</h1>
                    <h2>{{page.description}}</h2>
                </div>
        </header>
        <div class="container mx-auto px-4">
            <div class="inner">
                {{{page.html}}}
            </div>
        </div>
        <script src="/scripts/gloria.js"></script>
        <script src="/prism/prism.js"></script>
    </body>
</html>
