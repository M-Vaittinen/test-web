### Configuration:

Configuration options may want to enable for kernel build are:


```
{%- for c in page.configs %}
- {{ c.conf }}
{% endfor -%}
```

Description:
{%- for c in page.configs %}
{{ c.conf }}

{{ c.description }}

Subsystem: {{ c.subsystem }}
{% endfor -%}


