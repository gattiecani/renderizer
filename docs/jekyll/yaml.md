---
mylist:
  - firstkey: firstvalue
  - secondkey: secondvalue
---

{% for thing in page.mylist %}
{{ thing[0] }}: {{ thing[1] }}
  {% for hash in thing %}
- {{hash[0]}}: {{hash[1]}}
  {% endfor %}
{% endfor %}

{% include footer.md %}
