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

# Favorite Recipes

{% assign recipes_by_category = site.recipes | group_by: 'category' | sort: 'name' %}
{% for category_group in recipes_by_category %}
  <h3>{{ category_group.name }}</h3>
  <ul>
    {% assign sorted_recipes = category_group.items | sort: 'title' %}
    {% for recipe in sorted_recipes %}
      <li><a href="{{ recipe.url }}">{{ recipe.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

# Family
[Derrell Mervyn Charles Ireton - Obituary](_family/derrell_mervyn_charles_ireton_obituary.md)