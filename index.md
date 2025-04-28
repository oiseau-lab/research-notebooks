---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---

Homepage for [oiseau-lab](https://github.com/oiseau-lab)'s GitHub Pages of the [research-notebooks repository](https://github.com/oiseau-lab/research-notebooks).

Testing the formatting of a table imported from `.csv` format using Liquid below.

<table>
  {% for row in site.data.ERNAttributeDefinition %}
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