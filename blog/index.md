<!-- ---
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
</ul> -->
---
layout: page
title: Blog
permalink: /blog/
---

<style>
  .categories-container {
    display: flex;
    justify-content: space-between;
  }

  .category {
    width: 48%; /* Adjust the width as needed */
    border: 1px solid #ddd; /* Border around each category */
    padding: 20px;
    margin-bottom: 20px;
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

<div class="categories-container">
  {% for category in site.categories %}
    <div class="category">
      <h3>{{ category[0] }}</h3>
      <hr> <!-- Horizontal line under category name -->
      <ul class="posts-list">
        {% for post in category[1] %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>
