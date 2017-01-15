{% for data in site.data.dates %}- {{ data.data | date: "%Y" }}  
{% endfor %}
