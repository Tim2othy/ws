---
layout: page
title: Drafts
permalink: /drafts/
---

{% if site.drafts and site.drafts.size > 0 %}
{% assign drafts_alpha = site.drafts | sort: 'path' %}
<ul class="posts-list">
  {% for draft in drafts_alpha %}
  {% assign draft_name = draft.title | default: draft.basename %}
  <li>
    <a href="{{ draft.url | relative_url }}">{{ draft_name | escape }}</a>
  </li>
  {% endfor %}
</ul>
{% else %}
No drafts are available in this build.
{% endif %}
