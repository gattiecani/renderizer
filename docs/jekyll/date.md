{% for d in site.data.dates %}- {{ d.data | date: "%B %-d %Y" }}  
{% endfor %}
