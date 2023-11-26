---
layout: page
title: Blog
permalink: /blog/
---

<style>
  .categories-list {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 0;
  }

  .category {
    width: 48%; /* Adjust the width as needed */
    border-bottom: 1px solid #ddd; /* Line between categories */
    padding-bottom: 10px;
    margin-bottom: 20px;
    position: relative;
  }

  .category:last-child {
    border-bottom: none; /* Remove line for the last category */
  }

  .category h3 {
    margin-bottom: 10px;
  }

  .blur-bg {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    filter: blur(5px); /* Adjust the blur effect as needed */
  }
</style>

<ul class="categories-list">
  {% for category in site.categories %}
    <li class="category">
      <h3>{{ category[0] }}</h3>
      <div class="blur-bg"></div> <!-- Blur effect background -->
      <ul>
        {% for post in category[1] %}
          <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
