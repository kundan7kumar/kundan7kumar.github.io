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
  .container {
    display: flex;
  }

  .category-container {
    flex: 1;
    margin-right: 20px;
  }

  .categories {
    position: sticky;
    top: 0;
    width: 150px;
    background-color: white;
    border-right: 1px solid #ddd; /* Border between categories and posts */
    filter: blur(2px); /* Apply blur effect */
    padding: 20px;
  }

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

<div class="container">
  <div class="category-container">
    <div class="categories">
      {% for category in site.categories %}
        <div class="category">
          <h3>{{ category[0] }}</h3>
        </div>
      {% endfor %}
    </div>
  </div>

  <div class="posts-container">
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
  </div>
</div>
