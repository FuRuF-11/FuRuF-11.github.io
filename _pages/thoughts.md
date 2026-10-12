---
layout: default
permalink: /thoughts/
title: Thought
nav: true
nav_order: 2
---

<div class="post">
  <div class="header-bar">
    <h1>Thought</h1>
    <h2>Essays, ideas and random thoughts.</h2>
  </div>

  <ul class="post-list">
    {% assign thoughts = site.thoughts | sort: "date" | reverse %}
    {% for post in thoughts %}
      {% assign read_time = post.content | strip_html | number_of_words: "auto" | divided_by: 300 | plus: 1 %}
      <li>
        <h3>
          <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        {% if post.description != blank %}
          <p>{{ post.description }}</p>
        {% endif %}
        <p class="post-meta">
          {{ read_time }} min read &nbsp; &middot; &nbsp;
          {{ post.date | date: '%B %d, %Y' }}
        </p>
      </li>
    {% endfor %}
  </ul>
</div>
