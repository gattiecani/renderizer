---
title: "Generators"
generators:
  list:
    - 1
    -
      &giro zii:
        zio: 1
        zia: 0
  item_list:
    &pro list_1:
      - 1
      - 2
      - 3
    maps:
      -
        pro1: *pro
        pro2: 1
      -
        pro1:
          - cugino
          - cugina
          - *giro
        pro2: 2
---

# Generators

``` liquid
{% raw %}{% include filter.html table=page.generators %}{% endraw %}
```

{% include filter.html table=page.generators %}

{% include footer.md %}
