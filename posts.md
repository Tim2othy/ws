---
layout: page
title: Posts
permalink: /posts/
---

{% if site.posts and site.posts.size > 0 %}
<ul class="posts-list">
  {% assign posts_desc = site.posts | sort: 'date' | reverse %}
  {% for post in posts_desc %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    <span class="posts-list-date">{{ post.date | date: "%B %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
No posts yet.
{% endif %}

<p><a href="{{ '/drafts/' | relative_url }}">View drafts</a></p>
