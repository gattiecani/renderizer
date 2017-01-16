## Home

<ul>
{% assign navigation_pages = (site.html_pages | sort: "url") %}
{% for p in navigation_pages %}
        {% capture slug    %}{{ p.url | split: "/"   | last                       }}{% endcapture %}
  <li><a href="{{ p.url | absolute_url }}" {% if p.url == page.url %}class="link-gray"{% endif %}>{{ slug | upcase }} [{{p.url|split:'/' | join: '-'}}]</a>{{ current }}</li>
{% endfor %}
</ul>

{% include footer.md p=page %}
