---
layout: default
title: Think-Aloud
---

# Think-Aloud

Welcome. This is a small space for:

- **number and ideas** – playful math, patterns, and thoughts  
- **postcards** – little scenes, notes, and letters  
- **quiet words** – softer pieces and slower reflections  

You can also jump straight to:

- [number and ideas](/number-and-ideas/)
- [postcards](/postcards/)
- [quiet words](/quiet-words/)

---

## number and ideas

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

---

## postcards

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
<p><em>Empty mailbox for now.</em></p>
{% endif %}

---

## quiet words

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
<p><em>Silence, for the moment.</em></p>
{% endif %}
