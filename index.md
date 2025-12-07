---
# YAML Front Matter (Required for Jekyll Processing)
layout: default # or 'home'—depends on your theme. 'default' is safest.
title: My Awesome New Blog - Home
description: "Thoughts, code, and adventures from my iPad."
---

# Welcome to the Blog!

This is the main introduction to your blog. It will appear before the feed of posts.

---

<ul class="post-list">
  {% for post in site.posts limit: 10 %} 
  
  <li class="post-item">
    
    <h2><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h2>

    <span class="post-meta">
      Posted: {{ post.date | date: "%B %-d, %Y" }}
      {% if post.author %} - by {{ post.author }}{% endif %}
    </span>
    
    <div class="post-excerpt">
      {{ post.excerpt }}
    </div>

    <a href="{{ post.url | relative_url }}" class="read-more-link">Continue Reading &rarr;</a>
    
    <hr>
  </li>
  
  {% endfor %}
</ul>

