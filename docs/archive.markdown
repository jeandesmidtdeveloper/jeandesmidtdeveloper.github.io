---
layout: page
title: Archive
permalink: /archive/
---

{% assign categories = site.categories | sort %}

{% for category in categories %}
  <h2 id="{{ category[0] }}">{{ category[0] | capitalize }}</h2>

  <ul>
    {% for post in category[1] %}
      <li>
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
        <small>
          {{ post.date | date: "%Y-%m-%d" }}
        </small>
      </li>
    {% endfor %}
  </ul>
{% endfor %}