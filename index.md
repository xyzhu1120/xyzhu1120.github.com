---
layout: page
title: Little Pig!
tagline: xyz's blog
--
{% include JB/setup %}

{% for post in site.posts %}
  <div>
  <p><h2><a href="{{ BASE_PATH }}{{post.url}}">{{post.title}}</a></h2>{{ post.date | date_to_string }}</p>
  <p><a href="{{ BASE_PATH }}{{post.url}}">Read more ...</a></p>
  </div>
{% endfor %}
