{% for d in site.data.dates %}- {{ d | inspect }} `%B %-d %Y` {{ d.data | date: "%B %-d %Y" }}  
{% endfor %}

{% include footer.md %}
