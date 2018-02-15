{% for v in site.github.versions %}- {{ v[0] }}: {{ v[1] }}
{% endfor %}

{% include footer.md %}
