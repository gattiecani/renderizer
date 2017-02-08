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

{{ page.tags | inspect }}

## Push

Add as last.

```liquid
{% raw %}{{ page.tags | push: 'Spokane' | inspect }}{% endraw %}
```

Should render: ['Seattle', 'Tacoma', 'Spokane']

{{ page.tags | push: 'Spokane' | inspect }}

## Pop

Take the first.

```liquid
{% raw %}{{ page.tags | pop | inspect }}{% endraw %}
```

Should render: ['Seattle']

{{ page.tags | pop | inspect }}

## Shift

Take the last.

```liquid
{% raw %}{{ page.tags | shift | inspect }}{% endraw %}
```

from {{ page.tags | inspect }}

{{ page.tags | shift | inspect }}

Should render: ['Tacoma']

## Unshift

Add as first.

```liquid
{% raw %}{{ page.tags | unshift: "Olympia" | inspect }}{% endraw %}
```

Return: {{ page.tags | unshift: "Olympia" | inspect }}

Should be: ['Olympia', 'Seattle', 'Tacoma']

{% include footer.md %}
