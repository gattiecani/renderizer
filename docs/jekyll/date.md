{% for d in site.data.dates %}- {{ d | inspect }} `%B %-d %Y` {{ d.data | date: "%B %-d %Y" }}  
{% endfor %}

# {{ site.time | date: "%U" }}

{% include footer.md %}
