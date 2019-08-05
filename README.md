## Welcome to my site

...under construction...

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


<div class="toc">
  <ul class="post">
  <h1>My Blog</h1>
  {% capture written_year %}'None'{% endcapture %}
  {% for item in site.texts do %}
       {% capture year %}{{ item.date | date: '%Y' }}{% endcapture %}
    {% if year != written_year %}
      <h2>{{ year }}</h2>
      {% capture written_year %}{{ year }}{% endcapture %}
    {% endif %}
    <article>
      {% if item.link %}
        <li class="post-title">
          <a href="{{ site.baseurl }}{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a> <a href="{{ item.link }}" target="_blank" title="{{ item.title }}"><i class="fa fa-link"></i></a></li>
      {% else %}
        <li><a href="{{ site.baseurl }}{{ item.url }}" title="{{ item.title }}">{{ item.title }}</a> &#8212; <i><small>{{ item.excerpt | strip_html | truncate: 160 }}</small></i></li>
      {% endif %}
    </article>
  {% endfor %}
    </ul>
</div>
