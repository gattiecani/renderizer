## rb

```rb
Calendars: 5
Characters: 8
Locations: 3
```

## liquid

```liquid
{% raw %}{% include "maps/map.html" name="xkcd" %}{% endraw %}
```

ok

```liquid
{% raw %}{% include "maps/map.html" name="Nazzano" %}{% endraw %}
```

ok

```liquid
{% raw %}{% include "maps/map.html" name="nazzano" %}{% endraw %}
```

ok

```liquid
{% raw %}{% include "maps/map.html" name="xkcd" %}{% endraw %}
{% raw %}{% include "maps/map.html" name="Nazzano" %}{% endraw %}
{% raw %}{% include "maps/map.html" name="nazzano" %}{% endraw %}
```

ok

{% highlight liquid %}
{% raw %}{% include "maps/map.html" name="xkcd" %}{% endraw %}
{% raw %}{% include "maps/map.html" name="Nazzano" %}{% endraw %}
{% raw %}{% include "maps/map.html" name="nazzano" %}{% endraw %}
{% endhighlight %}
