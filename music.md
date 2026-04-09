---
layout: page
title: Music
permalink: /music/
---

All my music reviews.

{% for post in site.categories.music %}
  <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
{% endfor %}
