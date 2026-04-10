---
layout: page
title: Thoughts
permalink: /thoughts/
---

<div class="hero-block hero-block-small">
  <p class="hero-kicker">Thoughts</p>
  <h1 class="hero-title">Short writing, observations, and things that catch my attention.</h1>
  <p class="hero-text">
    Not everything needs to be long. Some things just need a place to land.
  </p>
</div>

<div class="post-feed">
  {% assign sorted_posts = site.categories.thoughts | sort: "date" | reverse %}
  {% for post in sorted_posts %}
    <article class="post-card">
      <p class="post-label">Thoughts</p>
      <h2 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <p class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 170 }}</p>
      <a class="read-more" href="{{ post.url | relative_url }}">Read entry</a>
    </article>
  {% endfor %}
</div>
