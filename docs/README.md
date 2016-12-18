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
{{c}}
**files**
  {% for p in c.files %}
- {{ p }}
  {% endfor %}
**docs**
  {% for d in c.docs %}
- {{ d }}
  {% endfor %}
{% endfor %}

### javascript
{% assign sorted_blog = (site.javascript | sort: 'date' | reverse) %}
{{ sorted_blog }}
{% for j in sorted_blog %}
{{ j }}
{% endfor %}
