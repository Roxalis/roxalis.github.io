---
layout: page
title: Welcome to my blog
---

<ul>
  {% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}<i><small> &#8212; {{ post.excerpt | strip_html | truncate: 160 }}, {{ year }}</small></i></a>  
    </li>
  {% endfor %}
</ul>
