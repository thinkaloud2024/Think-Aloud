---
layout: default
title: number and ideas
permalink: /number-and-ideas/
---

# number and ideas

{% assign number_posts = site.posts | where_exp: "post", "post.categories contains 'number-and-ideas'" %}
{% if number_posts.size > 0 %}
<ul>
  {% for post in number_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span> · {{ post.date | date: "%b %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
<p><em>Nothing here yet.</em></p>
{% endif %}
