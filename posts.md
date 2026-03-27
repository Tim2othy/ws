---
layout: page
title: Posts
permalink: /posts/
---

{% if site.posts and site.posts.size > 0 %}
<ul class="posts-list">
  {% assign posts_asc = site.posts | sort: 'date' %}
  {% for post in posts_asc %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    <span class="posts-list-date">{{ post.date | date: "%B %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
No posts yet.
{% endif %}
