# HOME

## Steps

1. Create a repository (or navigate to an existing repository)
1. Commit a Markdown file via the web interface, just like you would any other file
1. Activate GitHub Pages via your repository's settings

## Links

- [forms](forms)
- [scaffolding](scaffolding)

## Pages

{% assign navigation_pages = site.html_pages %}
{% for p in navigation_pages %}
{{ p }}
{% endfor %}
