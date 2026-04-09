---
layout: page
title: Thoughts
permalink: /thoughts/
---

Short posts and observations.
{% for post in site.categories.thoughts %}
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
{% endfor %}
