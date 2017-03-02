---
layout: default
permalink: /blog
title: Blog
---

<section class="post-list">
  {% for post in paginator.posts %}
    {% include article.html %}
  {% endfor %}

  {% include pagination.html %}
</section>