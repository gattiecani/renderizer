# HOME

- {{ site.github.build_revision }}
- [{{ site.github.repository_nwo }}]({{ site.github.repository_url }})

## Steps

1. Create a repository (or navigate to an existing repository)
1. Commit a Markdown file via the web interface, just like you would any other file
1. Activate GitHub Pages via your repository's settings

## Links

- [forms](forms)
- [scaffolding](scaffolding)

## Pages

<ul>
{% assign navigation_pages = site.html_pages %}
{% for p in navigation_pages %}
  <li><a href="{{ p.url | absolute_url }}" {% if p.url == page.url %}class="active"{% endif %}>{{ p.title | upcase }}</a></li>
{% endfor %}
</ul>

## Collections

{% for c in site.collections %}
### {{ c.label }}
  {% for p in c %}
- {{ p.path }}
  {% endfor %}
{% endfor %}
