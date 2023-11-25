---
layout: page
title: Blog
permalink: /blog/
---

<!-- Navigation Buttons -->
<div>
  {% for category in site.categories %}
    <a href="#{{ category[0] }}">{{ category[0] }}</a>
  {% endfor %}
</div>

<!-- Blog Categories and Posts -->
<ul>
  {% for category in site.categories %}
    <li>
      <h3 id="{{ category[0] }}">{{ category[0] }}</h3>
      <ul>
        {% for post in category[1] %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>

<!-- Add Anchor Tags for Each Category Section: -->
{% for category in site.categories %}
  <div id="{{ category[0] }}">
    <h2>{{ category[0] }}</h2>
    <ul>
      {% for post in category[1] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
