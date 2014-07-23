---
layout: default
---

{% for page in site.pages %}
{% if page.project == true %}
<entry>
   <a href="{{ page.url }}"/>{{ page.title }}</a>
 </entry>
{% endif %}
{% endfor %}


http://stackoverflow.com/questions/17118551/generating-a-list-of-pages-not-posts-in-a-given-category