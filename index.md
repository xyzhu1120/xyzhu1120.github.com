---
layout: page
title: Hello World!
tagline: Supporting tagline
---
{% include JB/setup %}

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)

## Update Author Attributes

In `_config.yml` remember to specify your own data:
    
    title : My Blog =)
    
    author :
      name : Name Lastname
      email : blah@email.test
      github : username
      twitter : username

{% for post in site.posts %}
	<div>
	<p><h2><a href="{{ BASE_PATH }}{{post.url}}">{{post.title}}</a></h2>{{ post.date | date_to_string }}</p>
	<p><a href="{{ BASE_PATH }}{{post.url}}">Read more ...</a></p>
	</div>
{% endfor %}
