### Configuration:

Configuration options may want to enable for kernel build are:


```
{%- for c in page.configs %}
- {{ c.config }}
{% endfor -%}
```

| config | description | subsystem |
------------------------------------
{%- for c in page.configs %}
| {{ c.config }} | {{ c.description }} | {{ c.subsystem }} |
{% endfor -%}


