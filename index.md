---
# layout: default
title: "Accueil"
---

{% for post in site.posts %}
{% assign day_index = post.date | date: "%w" | plus:0 | default: 0 %}
{% assign month_index = post.date | date: "%-m" | minus: 1 | default:0 %}

- [{{ post.title }}]({{ post.url }}) -
  {{ site.data.locale_fr.days[day_index] }}
  {{ post.date | date: "%d" }}
  {{ site.data.locale_fr.months[month_index] }}
  {{ post.date | date: "%Y" }}
  {% endfor %}

# Bienvenue sur ce qui n'est pas un site !

Voici la page principale de ce qui n'est pas un site.

[Aller au blog](./blog)
