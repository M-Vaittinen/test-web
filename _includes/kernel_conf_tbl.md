### Configuration:

Configuration options may want to enable for kernel build are:


```
{% for c in page.configs -%}
- {{ c.config }}
{% endfor -%}
```

| config | description | subsystem |
---------|-------------|-----------|
{% for c in page.configs -%}
{%- if c.description -%}
    {%- capture desc -%} {{ c.description }} {%- endcapture -%}
{%- else -%}
    {%- capture desc -%} {%- include {{ c.subsystem }}-cfg-desc.md -%} {%- endcapture -%}
{%- endif -%}
| {{ c.config }} | {{ desc }} | {{ c.subsystem }} |
{% endfor -%}


