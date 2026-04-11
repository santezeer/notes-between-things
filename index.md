---
layout: page
title: Home
permalink: /
---

<div class="hero-block">
  <p class="hero-kicker">Notes Between Things</p>
  <h1 class="hero-title">Music, thoughts, and whatever stays with me.</h1>
  <p class="hero-text">
    A personal space for album reviews, small observations, and things I want to put into words.
  </p>
</div>

<div class="post-feed">
  {% assign sorted_posts = site.posts | sort: "date" | reverse %}
  {% for post in sorted_posts %}
    <article class="post-card">


      <p class="post-label">{{ post.category }}</p>

      <h2 class="post-card-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h2>

      <p class="post-card-date">{{ post.date | date: "%B %d, %Y" }}</p>

      <p class="post-card-excerpt">
        {{ post.excerpt | strip_html | truncate: 100 }}
      </p>

      <a class="read-more" href="{{ post.url | relative_url }}">Read entry</a>

    </article>
  {% endfor %}
</div>
