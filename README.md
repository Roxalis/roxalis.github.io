## Welcome to my site

...under construction...

<ul>
  {% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  <h2>{{ year }}</h2>
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>&#8212; <i><small>{{ post.excerpt | strip_html | truncate: 160 }}</small></i>
    </li>
  {% endfor %}
</ul>


<div class="toc">
  <ul class="post">
  <h1>My Blog</h1>
  {% capture written_year %}'None'{% endcapture %}
  {% for post in site.posts do %}
       {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
    {% if year != written_year %}
      <h2>{{ year }}</h2>
      {% capture written_year %}{{ year }}{% endcapture %}
    {% endif %}
    <article>
      {% if post.link %}
        <li class="post-title">
          <a href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> <a href="{{ post.link }}" target="_blank" title="{{ post.title }}"><i class="fa fa-link"></i></a></li>
      {% else %}
        <li><a href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a> &#8212; <i><small>{{ post.excerpt | strip_html | truncate: 160 }}</small></i></li>
      {% endif %}
    </article>
  {% endfor %}
    </ul>
</div>
