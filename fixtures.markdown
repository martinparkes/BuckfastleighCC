---
layout: page
title: Fixtures
permalink: /fixtures/
---

# 2022

<table>
  {% for row in site.data.2022_fixtures %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>