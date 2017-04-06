layout 	title page
	
Tags
{% assign sorted-tags = site.tags | sort %}
{% for tag in sorted-tags %} {{ tag[0] }} {% endfor %}
{% for tag in sorted-tags %}
{{ tag[0] }}

<ul>
  {% for post in tag[1] %}
    <a class="tag-post" href="{{ site.baseurl }}{{ post.url }}">
	  <li>
		{{ post.title }}
	  <small class="post-date">{{ post.date | date_to_string }}</small>
	  </li>
    </a>
  {% endfor %}
</ul>

{% endfor %}

