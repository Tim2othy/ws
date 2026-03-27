---
layout: page
title: Drafts
permalink: /drafts/
---

{% assign drafts_alpha = site.collections['drafts'].docs | sort: 'path' %}

{% if drafts_alpha and drafts_alpha.size > 0 %}
<ul class="posts-list">
  {% for draft in drafts_alpha %}
  {% assign draft_name = draft.title | default: draft.basename %}
  <li>
    <a href="{{ draft.url | relative_url }}">{{ draft_name | escape }}</a>
  </li>
  {% endfor %}
</ul>
{% else %}
No drafts yet.
{% endif %}
