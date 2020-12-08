## rb

```rb
Calendars: 5
Characters: 8
Locations: 3
```

## liquid

Try single quote

```liquid
{% raw %}{% include 'maps/map.html' name="xkcd" %}{% endraw %}
```

Try liquid highlight

{%- highlight liquid -%}
{% raw %}{% include maps/map.html name="Nazzano" %}{% endraw %}
{% raw %}{% include 'maps/map.html' name="nazzano" %}{% endraw %}
{%- endhighlight -%}

Try Kramdown `{:.language-liquid}`

```
{% raw %}{% include maps/map.html name="xkcd" %}  
{% include 'maps/map.html' name="Nazzano" %}{% endraw %}
```
{:.language-liquid}

{% include footer.md %}
