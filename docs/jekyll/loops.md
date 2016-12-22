{% for i in (1..10) %}
`i` – {{ i }}
`length` – {{ forloop.length }}
`index` – {{ forloop.index }}
`index0` – {{ forloop.index0 }}
`rindex` – {{ forloop.rindex }}
`rindex0` – {{ forloop.rindex0 }}
`first` – {{ forloop.first }}
`last` – {{ forloop.last }}
{% endfor %}
