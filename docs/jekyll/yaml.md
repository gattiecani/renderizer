---
mylist:
  - firstkey: firstvalue
  - secondkey: secondvalue
---

{% for thing in page.mylist %}
{{ thing | inspect }}
  {% for hash in thing %}
- {{hash[1]}}
- {{hash[0]}}
  {% endfor %}
{% endfor %}
