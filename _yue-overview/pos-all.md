---
layout: base
title:  'POS tags'
generated: 'true'
permalink: yue/pos/all.html
udver: '2'
---

# POS tags

{% include yue-pos-table.html %}

----------

{% assign sorted = site.yue-pos | sort: 'title' %}{% for p in sorted %}
<a id="al-yue-pos/{{ p.title }}" class="al-dest"/>
<h2><code>{{ p.title }}</code>: {{ p.shortdef }}</h2>
{% if p.content contains "<!--details-->" %}    
{{ p.content | split:"<!--details-->" | first }}
<a href="{{ p.title }}" class="al-doc">See details</a>
{% else %}
{{ p.content }}
{% endif %}
<a href="{{ site.git_edit }}/{% if p.collection %}{{ p.relative_path }}{% else %}{{ p.path }}{% endif %}" target="#">edit {{ p.title }}</a>
{% endfor %}
