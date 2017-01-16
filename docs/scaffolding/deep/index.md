
```js
console.log('ok');
```
{% capture my_include %}{% include foo/index.md %}{% endcapture %}
{{ my_include | markdownify }}
