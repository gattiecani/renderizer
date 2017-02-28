## Loop `for i in (1..10)` with `forloop.`

<table style="text-align: center;">
<thead style="font-weight: bold;">
<tr>
<td>i</td>
<td>length</td>
<td>index</td>
<td>index0</td>
<td>rindex</td>
<td>rindex0</td>
<td>first</td>
<td>last</td>
</tr>
</thead>
<tbody>
{% for i in (1..10) %}
<tr>
<td>{{ i }}</td>
<td>{{ forloop.length }}</td>
<td>{{ forloop.index }}</td>
<td>{{ forloop.index0 }}</td>
<td>{{ forloop.rindex }}</td>
<td>{{ forloop.rindex0 }}</td>
<td>{{ forloop.first }}</td>
<td>{{ forloop.last }}</td>
</tr>
{% endfor %}
</tbody>
</table>

## Continue loop

Skip anything in the hidden_pages array, but keep looping over the rest of the values

{% assign hidden_pages = page.url %}
{% for page in site.pages %}{% if hidden_pages contains page.url %}{% continue %}{% endif %}
- [{{ page.title | default: page.name }}]({{page.url | absolute_url}}){% endfor %}

## Break loop

After we reach the "cutoff" page, stop the list and get on with whatever's after the "for" loop

{% assign cutoff_page = page.url %}
{% for page in site.pages %}
- [{{ page.title | default: page.name }}]({{page.url | absolute_url}}){% if cutoff_page == page.url %}{% break %}{% endif %}{% endfor %}

{% include footer.md %}
