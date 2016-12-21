{% for gig in site.data.cosmonauti.gigs %}
1. **{{gig.city}}** – {{gig.date | date_to_long_string}} @ {{gig.venue}}
{% endfor %}
