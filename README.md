<span style="display:block; height: 1px;"></span>
# Welcome To My Blog

<ul class="ex">
  {% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}<i> &#8212; {{ post.excerpt | strip_html | truncate: 160 }}, {{ year }}</i></a>  
    </li>
  {% endfor %}
</ul>
