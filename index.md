---
layout: default
title: "Scott Ireton"
---

# Projects

[Sum Calculator](calculator.html)

---

# Hawaii 2025

<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.date | date: "%B %d" }} – {{ post.title }}</a></li>
  {% endfor %}
</ul>

---

# Recipes

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

---

# Family
<!-- [Derrell Mervyn Charles Ireton - Obituary](family/derrell_mervyn_charles_ireton_obituary.html) -->

<ul>
  {% for post in site.family %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

---

# Quotes

<ul>
  {% for quote in site.quotes %}
    <li><a href="{{ quote.url }}">{{ quote.title }}</a></li>
  {% endfor %}
</ul>