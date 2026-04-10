---
layout: page
title: Music
permalink: /music/
---

<div class="hero-block hero-block-small">
  <p class="hero-kicker">Music</p>
  <h1 class="hero-title">Reviews, notes, and albums I keep returning to.</h1>
  <p class="hero-text">
    Personal writing about records that stood out to me, whether immediately or over time.
  </p>
</div>

<div class="post-feed">
  {% assign sorted_posts = site.categories.music | sort: "date" | reverse %}
  {% for post in sorted_posts %}
    <article class="post-card">
      <p class="post-label">Music</p>
      <h2 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>
      <p class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</p>
      <p class="post-card-excerpt">{{ post.excerpt | strip_html | truncate: 170 }}</p>
      <a class="read-more" href="{{ post.url | relative_url }}">Read review</a>
    </article>
  {% endfor %}
</div>
