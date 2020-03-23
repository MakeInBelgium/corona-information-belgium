---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<style type="text/css">
th, td {
  text-align: center;
}
</style>

<table>
<tr>
  <th colspan="2">taal</th>
  <th>preventie</th>
  <th colspan="2">maatregelen</th>
</tr>

{% for entry in site.data.data %}
<tr>
  <td>{{ entry.taal }}</td>
  <td>{{ entry.language }}</td>
  <td>{% if entry.prevention.phrase %}<a href="{{ entry.prevention.url }}">{{ entry.prevention.phrase }}</a>{% endif %}</td>
  <td>{% if entry.measures.pdf %}<a href="{{ entry.measures.pdf }}"><img src="pdf.svg" height="30"></a>{% endif %}</td>
  <td>{% if entry.measures.audio %}<a href="{{ entry.measures.audio }}"><img src="audio.svg" height="30"></a>{% endif %}</td>
</tr>
{% endfor %}

<p>Deze informatie is afkomstig van <a href="https://www.integratie-inburgering.be/corona-meertalige-info">Agentschap Integratie en Inburgering</a>, en voorziet enkel in een alternatieve weergave.

</table>
