---
layout: archive 
author_profile: true
header:
  overlay_image: header/jeju.jpeg
excerpt: "Publications"
---

{% for post in site.categories.pub %}
	{% include archive-pub-single.html %}
{% endfor %}


<!-- 
{% for post in paginator.posts %}
  {% if post.category == "blog" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% include paginator.html %}
--!>



