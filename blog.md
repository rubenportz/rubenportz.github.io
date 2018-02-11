---
layout: default
---
<!DOCTYPE html>
<html>	
  <body>
    <div class="container">
	   	{% for post in site.posts %}
		    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
		    <p>{{ post.content | strip_html | truncatewords:20 }}</p>
		    <p>{{ post.date | date: "%b %d, %Y" }} {% include read_time.html %} </p>
		{% endfor %} 		    
    </div>
  </body>	
</html>