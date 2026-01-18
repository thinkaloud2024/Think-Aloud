---
layout: default
title: Think-Aloud
---

Welcome. This is a small space for:

- **number and ideas** – playful math, patterns, and thoughts that almost click  
- **postcards** – little scenes, notes, and letters to nowhere in particular  
- **quiet words** – softer pieces and slower reflections  

<hr class="nav-divider" />

<ul class="nav-links">
  <li><a href="{{ "/number-and-ideas/" | relative_url }}">number and ideas</a></li>
  <li><a href="{{ "/postcards/" | relative_url }}">postcards</a></li>
  <li><a href="{{ "/quiet-words/" | relative_url }}">quiet words</a></li>
</ul>

---

## number and ideas

{% assign number_posts = site.posts | where_exp: "post", "post.categories contains 'number-and-ideas'" %}
{% if number_posts.size > 0 %}
<ul>
  {% for post in number_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a> · {{ post.date | date: "%b %d, %Y" }}
  </li>
  {% endfor %}
</ul>
{% endif %}

---

## postcards

{% assign postcard_posts = site.posts | where_exp: "post", "post.categories contains 'postcards'" %}
{% if postcard_posts.size > 0 %}
<ul>
  {% for post in postcard_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a> · {{ post.date | date: "%b %d, %Y" }}
  </li>
  {% endfor %}
</ul>
{% endif %}

---

## quiet words

{% assign quiet_posts = site.posts | where_exp: "post", "post.categories contains 'quiet-words'" %}
{% if quiet_posts.size > 0 %}
<ul>
  {% for post in quiet_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a> · {{ post.date | date: "%b %d, %Y" }}
  </li>
  {% endfor %}
</ul>
{% endif %}

