---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<div class="w3-mobile" markdown="1">

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

</div>
