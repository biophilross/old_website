---
layout: page
title: 
---

Blog

<!-- This loops through the paginated posts -->
<div class="posts">
  {% for post in paginator.posts %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>

    {{ post.content }}
  </div>
  {% endfor %}
</div>

<!-- Pagination links -->
<div class="pagination">
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Older</a>
  {% else %}
    <span class="next ">Older</span>
  {% endif %}
    {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="previous">Newer</a>
  {% else %}
    <span class="previous">Newer</span>
  {% endif %}
</div>

