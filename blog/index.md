---
layout: page
title: Blog
permalink: /blog/
---

<ul>
  {% for category in site.categories %}
    <li>
      <h3>{{ category[0] }}</h3>
      <ul>
        {% for post in category[1] %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
