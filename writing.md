---
layout: page
title: Writing
permalink: /writing/
---

{% comment %}
A post can link an accompanying paper by adding `paper: /papers/<name>/` to its
front matter. The paper's title is taken from that paper page.
{% endcomment %}

{% if site.posts and site.posts.size > 0 %}
<ul class="posts-list">
  {% assign posts_desc = site.posts | sort: 'date' | reverse %}
  {% for post in posts_desc %}
  <li>
    {% if post.paper %}
    {% assign paper_obj = site.pages | where: 'url', post.paper | first %}
    <div class="posts-list-row">
      <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      <span class="posts-list-paper">Paper: <a href="{{ post.paper | relative_url }}">{{ paper_obj.title | default: post.paper | escape }}</a></span>
    </div>
    {% else %}
    <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
    {% endif %}
    <span class="posts-list-date">{{ post.date | date: "%B %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
No posts yet.
{% endif %}

<p><a href="{{ '/drafts/' | relative_url }}">View drafts</a></p>
