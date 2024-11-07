---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: default
title: "Blog"
---

# Bienvenue sur ce qui n'est pas un blog !

Les derniers articles :
{% for post in site.posts %}

- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%d %B %Y"}}
  {% endfor %}
