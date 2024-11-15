### Configuration:

Configuration options may want to enable for kernel build are:


```
{%- for c in page.configs %}
- {{ c.config }}
{% endfor -%}
```

Description:
{%- for c in page.configs %}
{{ c.config }}

{{ c.description }}

Subsystem: {{ c.subsystem }}
{% endfor -%}


