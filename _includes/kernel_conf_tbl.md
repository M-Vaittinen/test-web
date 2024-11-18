---
test:
  - varrrr: Yay
    barrrr: it's all good
---
### Configuration:

Configuration options may want to enable for kernel build are:

I dont think the front matter in included file gets used :/
{% for t in page.test -%}
- {{ t.varrrr }}
- {{ t.barrrr }}
{% endfor -%}


```
{% for c in page.configs -%}
- {{ c.config }}
{% endfor -%}
```

| config | description | subsystem |
---------|-------------|-----------|
{% for c in page.configs -%}
| {{ c.config }} | {{ c.description }} | {{ c.subsystem }} |
{% endfor -%}


