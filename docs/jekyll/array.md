---
tags: ['Seattle', 'Tacoma']
---

# Array Filters

Array filters are [NON-DESTRUCTIVE](https://ashmaroli.github.io/jekyll/docs/templates/)

**Inspect page tags**

```liquid
{% raw %}{{ page.tags | inspect }}{% endraw %}
```

Should render: ["Seattle", "Tacoma"]

Render: {{ page.tags | inspect }}

## Push

Add as last.

```liquid
{% raw %}{{ page.tags | push: 'Spokane' | inspect }}{% endraw %}
```

Should render: ['Seattle', 'Tacoma', 'Spokane']

Render: {{ page.tags | push: 'Spokane' | inspect }}

## Pop

Take the first.

```liquid
{% raw %}{{ page.tags | pop | inspect }}{% endraw %}
```

Should render: ['Seattle']

Render: {{ page.tags | pop | inspect }}

## Shift

Take the last.

```liquid
{% raw %}{{ page.tags | shift | inspect }}{% endraw %}
```

from {{ page.tags | inspect }}

Should render: ['Tacoma']

Render: {{ page.tags | shift | inspect }}

## Unshift

Add as first.

```liquid
{% raw %}{{ page.tags | unshift: "Olympia" | inspect }}{% endraw %}
```

Should render: ['Olympia', 'Seattle', 'Tacoma']

Render: {{ page.tags | unshift: "Olympia" | inspect }}

{% include footer.md %}
