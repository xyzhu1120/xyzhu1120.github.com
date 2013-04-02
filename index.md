---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

{% for post in site.posts %}
  <div>
  <p><h2><a href="{{ BASE_PATH }}{{post.url}}">{{post.title}}</a></h2>{{ post.date | date_to_string }}</p>
  <p><a href="{{ BASE_PATH }}{{post.url}}">Read more ...</a></p>
  </div>
{% endfor %}
