
### arr md:

{{ page.configs | inspect }}

{% for key in page.configs %}
 - {{ key }} - {{ page.configs[key] }}
{% endfor %}
