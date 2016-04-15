---
layout: page
title: Noms
---

<div class="posts">
  {% for post in site.categories.noms %}
  <div class="post">
    <h1 class="post-title">
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>

    <span class="post-date">{{ post.date | date_to_string }}</span>
    {{ post.content }}
    {% if post.comments %}
      <div class="wrapper wrapper-{{forloop.index}}">
        <button onclick="loadDisqus(jQuery(this), '{{ site.url }}{{ post.url }}', '{{ post.title }}')">Show comments</button>
      </div>
    {% endif %}
  </div>
  {% endfor %}
</div>
