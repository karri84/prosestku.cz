---
layout: page
title: Naši kandidáti 
description: When building a website it's helpful to see what the focus of your site is. This page is an example of how to show a website's focus.
sitemap:
    priority: 0.7
    lastmod: 2018-08-21
    changefreq: weekly
---

{% for person in site.data.people %}
{% if forloop.index < 6 %}
### {{person.position}}. {{ person.name }}
<div class="box">
<img class="image left" style="height: 200px;" src="/images/persons/{{  person.id }}.jpg" alt="{{ person.name }}" />
<b>Věk:</b> {{ person.age }}<br>
<b>Povolání:</b> {{ person.work }}<br>
<b>Část obce:</b> {{ person.citypart }}<br>
{{ person.party }}
<hr style="clear:left;">
</div>
{% else %}
<b>{{person.position}}. {{ person.name }},</b> {{person.age}} let, {{person.work}}, {{ person.citypart }}
{% endif %}
{% endfor %}
