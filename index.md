---
layout: base.njk
---

# Hello, world!

This is an [11ty](https://www.11ty.dev/) starter. It includes a basic blog, a few pages.

## Blog posts

{%- assign posts = collections.post | reverse -%}
{% for post in posts %}
- [{{ post.data.title }}]({{ post.url }})</li>
{% endfor %}