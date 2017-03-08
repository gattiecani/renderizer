---
mylist:
  - firstkey: firstvalue
  - secondkey: secondvalue
---

{% for thing in page.mylist %}
{{ thing | inspect }}
  {% for hash in thing %}
- {{hash[0]}}: {{hash[1]}}
  {% endfor %}
{% endfor %}

{% include footer.md %}
