---
tags: ['Seattle', 'Tacoma']
---

# Array

**Inspect page tags**

```liquid
{% raw %}{{ page.tags | inspect }}{% endraw %}
```

Should render: ["Seattle", "Tacoma"]

{{ page.tags | inspect }}

## Push

```liquid
{% raw %}{{ page.tags | push: 'Spokane' | inspect }}{% endraw %}
```

Should render: ['Seattle', 'Tacoma', 'Spokane']

{{ page.tags | push: 'Spokane' | inspect }}

## Pop

```liquid
{% raw %}{{ page.tags | pop | inspect }}{% endraw %}
```

Should render: ['Seattle']

{{ page.tags | pop | inspect }}

## Shift

```liquid
{% raw %}{{ page.tags | shift }}{% endraw %}
```

from {{ page.tags | inspect }}

Should render: ['Tacoma']

{{ page.tags | shift }}

## Unshift

```liquid
{% raw %}{{ page.tags | unshift: "Olympia" }}{% endraw %}
```

Return: {{ page.tags | unshift: "Olympia" }}

Should be: ['Olympia', 'Seattle', 'Tacoma']

{% include footer.md %}
