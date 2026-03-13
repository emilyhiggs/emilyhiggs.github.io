---
layout: page
title: writing
permalink: /writing/
nav: false
nav_order: 2
---

## Essays & Posts

{% if site.posts.size > 0 %}
<ul class="post-list">
{% for post in site.posts %}
  <li>
    <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.description %}
      — {{ post.description }}
    {% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p>Posts forthcoming.</p>
{% endif %}

---

## Publications

Peer-reviewed articles and contributed book chapters.

{% bibliography --query @* %}
