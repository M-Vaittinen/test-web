
{% for cfg in page.conf %}
- {{ cfg.config }} - {{ cfg.description }}. Subsystem {{ cfg.subsystem }}
{% endfor %}
