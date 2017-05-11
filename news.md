---
title: News
layout: default
permalink: /news/
---

<div style="padding-left:5%;padding-right:5%">
<ul>
  {% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{post.date | date: '%B %d, %Y'}} {{ post.title }}</a><br/>
    {{ post.content }}
    <br/>
    <br/>
  </li>
  {% endfor %}
</ul>
</div>
