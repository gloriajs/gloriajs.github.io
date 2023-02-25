---
permalink: /blog/
title: Blog
description: Blog posts or something
---
<h1>Blog</h1>

<ul class="posts-list">
  {{#each posts}}
    <li><a href="{{url}}"><strong>{{capitalize category}}</strong>: {{capitalize title}}</a></li>
  {{/each}}
</ul>
