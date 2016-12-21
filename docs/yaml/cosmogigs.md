{% for gig in site.data.cosmonauti %}
{{ gig.date | date: "%-d" }},{{ gig.date | date: "%-m" }},{{ gig.date | date: "%-Y" }},{{gig.city}},{{gig.venue}}
{% endfor %}
