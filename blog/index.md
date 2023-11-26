<!-- ---
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
{% endfor %} -->
---
layout: page
title: Blog
permalink: /blog/
---

<style>
  .container {
    display: flex;
    justify-content: space-between;
  }

  .categories {
    width: 20%;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.8); /* Adjust the alpha value for the blur effect */
    backdrop-filter: blur(5px); /* Apply blur effect */
  }

  .posts {
    width: 75%;
  }

  .category {
    margin-bottom: 20px;
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
  <div class="categories">
    {% for category in site.categories %}
      <div class="category">
        <h3>{{ category[0] }}</h3>
      </div>
    {% endfor %}
  </div>

  <div class="posts">
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
