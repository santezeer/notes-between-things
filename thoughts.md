---
layout: page
title: Thoughts
permalink: /thoughts/
---

<p class="section-intro">Short posts and observations.</p>

<div class="post-feed">
  {% for post in site.categories.thoughts %}
    <article class="post-card">
      <h2 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <p class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
      <a class="read-more" href="{{ post.url | relative_url }}">Read more</a>
    </article>
  {% endfor %}
</div>
