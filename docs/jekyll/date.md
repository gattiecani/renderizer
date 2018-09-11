Read dates from [`_data/dates.csv`](https://github.com/gattiecani/renderizer/blob/master/docs/_data/dates.csv) and print.

```liquid
{% raw %}{{ d.data | date: "%B %-d %Y" }}{% endraw %}
```

{% for d in site.data.dates %}- {{ d | inspect }} `%B %-d %Y` {{ d.data | date: "%B %-d %Y" }}  
{% endfor %}

### {{ site.time | date: "%s" }} `%s` Unix time

### {{ site.time | date: "%A" }} `%A` Full weekday name

### {{ site.time | date: "%U" }} `%U` Week number of the current year (start Sunday)

### {{ site.time | date: "%W" }} `%W` Week number of the current year (start Monday)

### {{ site.time | date: "%w" }} `%w` Day of the week (Sunday is 0)

# Now

{{ "now" | date_to_rfc822 }}

{% include footer.md %}
