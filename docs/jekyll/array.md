---
tags: ['Seattle', 'Tacoma']
---

**Inspect tags**

{{ page.tags | inspect }}

**Push**

```liquid
{% raw %}{{ page.tags | push: 'Spokane' }}{% endraw %}
```

{{ page.tags | push: 'Spokane' }}
{{ page.tags | inspect }}

Should be: ['Seattle', 'Tacoma', 'Spokane']

**Pop**

```liquid
{% raw %}{{ page.tags | pop }}{% endraw %}
```

{{ page.tags | pop }}
Should be: ['Seattle']

**Shift**

```liquid
{% raw %}{{ page.tags | shift }}{% endraw %}
```

{{ page.tags | shift }}
Should be: ['Tacoma']

**Unshift**

```liquid
{% raw %}{{ page.tags | unshift: "Olympia" }}{% endraw %}
```

{{ page.tags | unshift: "Olympia" }}
Should be: ['Olympia', 'Seattle', 'Tacoma']

{% include footer.md %}
