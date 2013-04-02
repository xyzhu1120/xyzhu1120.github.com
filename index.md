---
layout: page
title: HOME
tagline: xyz's blog
---
{% include JB/setup %}

{% for post in site.posts %}
  <div>
  <p><h2><a href="{{ BASE_PATH }}{{post.url}}">{{post.title}}</a></h2>{{ post.date | date_to_string }}</p>
  <p>{{ post.content | strip_html | truncatewords: 55}}</p>
  <p><a href="{{ BASE_PATH }}{{post.url}}">Read more ...</a></p>
  </div>
{% endfor %}
