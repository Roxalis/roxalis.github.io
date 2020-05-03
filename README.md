<span style="display:block; height: 10px;"></span>

# Welcome to my blog

<ul>
  {% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}<i> &#8212; {{ post.excerpt | strip_html | truncate: 160 }}, {{ year }}</i></a>  
    </li>
  {% endfor %}
</ul>
