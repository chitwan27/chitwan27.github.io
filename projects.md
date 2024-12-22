---
layout: page
title: Projects
description: "List Of All My Projects"
keywords: "blog, development, philosophy, society"
author: "Chitwan Singh"
---

<ul class="post-list">
  {% for post in site.projects %}
    <li>
      <a class='post-link' href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.content | strip_html | truncatewords: 75 }}</p>
    </li>
  {% endfor %}
</ul>