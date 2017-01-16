
```js
console.log('ok');
```
{% capture my_include %}{% include_relative foo/index.md %}{% endcapture %}
{{ my_include | markdownify }}
