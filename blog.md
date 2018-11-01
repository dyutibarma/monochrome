---
layout: page
title: Blog
description: Most recent blog posts.
---

{% for blog in site.blog %}
  <h3><a href="{{ blog.url }}">{{ blog.title }}</a></h3>
    <p><i>{{ blog.tags }}</i></p>
    <time datetime="{{ blog.date | date_to_xmlschema }}" class="by-line"> <i>{{ blog.date | date_to_string }}</i> </time>
      {{ blog.excerpt }}
{% endfor %}
