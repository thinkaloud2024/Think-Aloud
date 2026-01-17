---
layout: default
title: postcards
permalink: /postcards/
---

# postcards

{% assign postcard_posts = site.posts | where_exp: "post", "post.categories contains 'postcards'" %}
{% if postcard_posts.size > 0 %}
<ul>
  {% for post in postcard_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span> · {{ post.date | date: "%b %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
<p><em>No postcards sent yet.</em></p>
{% endif %}
