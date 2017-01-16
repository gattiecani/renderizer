# HOME

- repository: [{{ site.github.repository_nwo }}]({{ site.github.repository_url }})
- build: `{{ site.github.build_revision }}`

## Steps

1. Create a repository (or navigate to an existing repository)
1. Commit a Markdown file via the web interface, just like you would any other file
1. Activate GitHub Pages via your repository's settings

## Path

<ul>
{% assign navigation_pages = (site.html_pages | sort: "path" | reverse) %}
{% for p in navigation_pages %}
  <li><a href="{{ p.url | absolute_url }}" {% if p.url == page.url %}class="link-gray"{% endif %}>path: {{ p.path }} [{{p.path|split:'/' | join: '-'}}]</a></li>
{% endfor %}
</ul>

## Url

<ul>
{% assign navigation_pages = (site.html_pages | sort: "url") %}
{% for p in navigation_pages %}
        {% capture slug    %}{{ p.url | split: "/"   | last                       }}{% endcapture %}
        {% capture current %}{{ p.url | remove: slug | remove: "//" | append: "/" }}{% endcapture %}
  <li><a href="{{ p.url | absolute_url }}" {% if p.url == page.url %}class="link-gray"{% endif %}>{{ slug | upcase }} [{{p.url|split:'/' | join: '-'}}]</a>{{ current }}</li>
{% endfor %}
</ul>

<script type="text/javascript">
document.querySelector('body').classList.add('markdown-body');
</script>
