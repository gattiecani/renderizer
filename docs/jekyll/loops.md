## Loop `for i in (1..10)` with index

{% for i in (1..10) %}
- `i` – {{ i }}
- `length` – {{ forloop.length }}
- `index` – {{ forloop.index }}
- `index0` – {{ forloop.index0 }}
- `rindex` – {{ forloop.rindex }}
- `rindex0` – {{ forloop.rindex0 }}
- `first` – {{ forloop.first }}
- `last` – {{ forloop.last }}
{% endfor %}

## Continue & Break

Skip anything in the hidden_pages array, but keep looping over the rest of the values

{% assign hidden_pages = page.url %}
{% for page in pages %}
  {% if hidden_pages contains page.url %}
    {% continue %}
  {% endif %}
- [page.title](page.url)
{% endfor %}

After we reach the "cutoff" page, stop the list and get on with whatever's after the "for" loop

{% assign cutoff_page = page.url %}
{% for page in pages %}
- [page.title](page.url)
  {% if cutoff_page == page.url %}
    {% break %}
  {% endif %}
{% endfor %}

{% include footer.md %}
