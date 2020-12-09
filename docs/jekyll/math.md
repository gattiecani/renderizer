# Math

### `modulo`

Divides an output by a number and returns the remainder.

```liquid
{% raw %}{% 12 | modulo:5 %}{% endraw %}
2
```

### `round`

Rounds the output to the nearest integer or specified number of decimals.

```liquid
{% raw %}{{ 4.6 | round }}
{{ 4.3 | round }}
{{ 4.5612 | round: 2 }}{% endraw %}
{{ 4.6 | round }}
{{ 4.3 | round }}
{{ 4.5612 | round: 2 }}
```

### `floor`

Rounds an output down to the nearest integer.

```liquid
{% raw %}{{ 4.6 | floor }}{% endraw %}
{{ 4.6 | floor }}
{% raw %}{{ 4.3 | floor }}{% endraw %}
{{ 4.3 | floor }}
```

### `ceil`

Rounds an output up to the nearest integer.
```liquid
{% raw %}{{ 4.6 | ceil }}{% endraw %}
{{ 4.6 | ceil }}
{% raw %}{{ 4.3 | ceil }}{% endraw %}
{{ 4.3 | ceil }}
```
{% include footer.md %}
