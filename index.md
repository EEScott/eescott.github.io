---
layout: default
title: "Our Hawaii Trip"
---

# Our Hawaii Trip
Welcome to our travel journal! Click on a day to see what we were up to.

<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.date | date: "%B %d" }} – {{ post.title }}</a></li>
  {% endfor %}
</ul>

## Favorite Recipes

<ul>
  {% for recipe in site.recipes %}
    <li><a href="{{ recipe.url }}">{{ recipe.title }}</a></li>
  {% endfor %}
</ul>
