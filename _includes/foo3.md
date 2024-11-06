# FOOO 3

got model {{ page.model }} and flag {{ page.flag }}

{%- if supplies %}
{% for supply in supplies %}
    {{ supply }}-supply = <&{{ supply}}>;
{% endfor %}
{% else %}
no supplies
{% endif %}
