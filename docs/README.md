# HOME

- {{ site.github.build_revision }}
- [{{ site.github.repository_nwo }}]({{ site.github.repository_url }})

## Steps

1. Create a repository (or navigate to an existing repository)
1. Commit a Markdown file via the web interface, just like you would any other file
1. Activate GitHub Pages via your repository's settings

## Loop

<ul>
{% assign navigation_pages = (site.html_pages | sort: "path") %}
{% for p in navigation_pages %}
  <li><a href="{{ p.url | absolute_url }}" {% if p.url == page.url %}class="active"{% endif %}>title: {{ p.title }}, {{p.url|split:'/' | join: ', '}}</a></li>
{% endfor %}
{{cats}}
</ul>

## Navigation

{% include navigation.html context="/" %}

<script type="text/javascript">
document.querySelector('body').classList.add('markdown-body');
</script>
