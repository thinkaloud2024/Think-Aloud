---
layout: default
title: quiet words
permalink: /quiet-words/
---

# quiet words

{% assign quiet_posts = site.posts | where_exp: "post", "post.categories contains 'quiet-words'" %}
{% if quiet_posts.size > 0 %}
<ul>
  {% for post in quiet_posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span> · {{ post.date | date: "%b %d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
<p><em>Still gathering themselves.</em></p>
{% endif %}
