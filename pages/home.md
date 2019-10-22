---
layout: layouts/layout.html
pageTitle: Welcome
tags:
  - nav
navTitle: Home
date: 2019-01-01
permalink: /
---

<section>
  
  {% for post in collections.posts %}
  <article>
  {{ post.templateContent }}
  {{ post.date | date: "%Y-%m-%d" }}
  </article>
  {% endfor %}
  
</section>

<section>

{% for post in collections.posts %}

  <article>
  <h2><a href="{{ post.url }}">{{ post.data.postTitle | upcase }}</a></h2>
  <p>{{ post.date | date: "%Y-%m-%d" }}<p>
  </article>
  {% endfor %}

</section>
