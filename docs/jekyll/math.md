---
---

# Math

### `modulo`

Divides an output by a number and returns the remainder.

```liquid
{{ raw }}{{ 12 | modulo:5 }}{{ endraw }}
2
```

### `round`

Rounds the output to the nearest integer or specified number of decimals.

```liquid
{{ raw }}{{ 4.6 | round }}{{ endraw }}
{{ raw }}{{ 4.3 | round }}{{ endraw }}
{{ raw }}{{ 4.5612 | round: 2 }}{{ endraw }}
5
4
4.56
```

### `floor`

Rounds an output down to the nearest integer.

```jekyll
{{ raw }}{{ 4.6 | floor }}{{ endraw }}
{{ raw }}{{ 4.3 | floor }}{{ endraw }}
4
4
```

### `ceil`

Rounds an output up to the nearest integer.
```liquid
{{ raw }}{{ 4.6 | ceil }}{{ endraw }}
{{ raw }}{{ 4.3 | ceil }}{{ endraw }}
5
5
```
{% include footer.md %}
