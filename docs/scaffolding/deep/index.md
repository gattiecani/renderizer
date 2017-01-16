
```js
console.log('ok');
```
{% capture my_include %}{% include README.md %}{% endcapture %}
{{ my_include | markdownify }}
