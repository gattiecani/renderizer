---
---

# Math

### `round`

Rounds the output to the nearest integer or specified number of decimals.

```liquid
{{ 4.6 | round }}
{{ 4.3 | round }}
{{ 4.5612 | round: 2 }}
5
4
4.56
```

### `floor`

Rounds an output down to the nearest integer.

```jekyll
{{ 4.6 | floor }}
{{ 4.3 | floor }}
4
4
```

### `ceil`

Rounds an output up to the nearest integer.
```liquid
{{ 4.6 | ceil }}
{{ 4.3 | ceil }}
5
5
```
{% include footer.md %}
