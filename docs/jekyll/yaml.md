---
mylist:
  - firstkey: firstvalue
  - secondkey: secondvalue
---

{% for thing in page.mylist %}
{{ thing[1] | append: ' : ' | append: thing[0] }}
  {% for hash in thing %}
- {{hash[0]}}
- {{hash[1]}}
  {% endfor %}
{% endfor %}
