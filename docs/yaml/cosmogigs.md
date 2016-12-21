{% for gig in site.data.cosmonauti %}
1. **{{gig.city}}** – {{gig.date | date_to_long_string}} @ {{gig.venue}}
{% endfor %}
