{% for d in site.data.dates %}- {{ d | inspect }} `%B %-d %Y` {{ d.data | date: "%B %-d %Y" }}  
{% endfor %}

### {{ site.time | date: "%s" }} `%s` Unix time

### {{ site.time | date: "%A" }} `%A` Full weekday name

### {{ site.time | date: "%U" }} `%U` Week number of the current year (start Sunday)

### {{ site.time | date: "%W" }} `%W` Week number of the current year (start Monday)

### {{ site.time | date: "%w" }} `%w` Day of the week (Sunday is 0)

{% include footer.md %}
