---
layout: page
title: Blog
permalink: /blog/
---

-----------------------
<style>
  .category {
    border-bottom: 1px solid #ddd; /* Border between categories */
    padding-bottom: 20px; /* Space between category name and posts */
  }

  .category h3 {
    margin-bottom: 10px;
  }

  .posts-list {
    list-style: none;
    padding: 0;
  }

  .posts-list li {
    margin-bottom: 10px;
  }
</style>

{% for category in site.categories %}
  <div class="category">
    <h3>{{ category[0] }}</h3>
    <ul class="posts-list">
      {% for post in category[1] %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
