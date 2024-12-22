---
layout: page
title: Blogroll
description: "List Of All Posts"
keywords: "blog, development, philosophy, society"
author: "Chitwan Singh"
---

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        {{ post.date | date: date_format }}
      </time>
      <a class='post-link' href="{{ post.url }}">{{ post.title }}</a>
      <p>{{ post.content | strip_html | truncatewords: 125 }}</p>
    </li>
  {% endfor %}
</ul>