---
layout: default
title: Think-Aloud
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

  {% endfor %}
</ul>
{% endif %}

