<span style="display:block; height: 1px;"></span>
# Welcome to my blog!

"*I'm not kidding. The arts are not a way to make a living. They are a very human way of making life more bearable. Practicing an art, no matter how well or badly, is a way to make your soul grow, for heaven's sake.*" - Kurt Vonnegut

<ul class="ex1">
  {% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}<i> &#8212; {{ post.excerpt | strip_html | truncate: 160 }}, {{ year }}</i></a>  
    </li>
  {% endfor %}
</ul>
