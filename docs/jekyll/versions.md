{% for v in site.github.versions %}
- {{ v[0] }}: {{ v[1] }} {{ v | inspect }}
{% endfor %}

{% include footer.md %}
