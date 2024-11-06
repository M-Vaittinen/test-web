---
permalink: /
model: my-model
flag: my-flag
test: [ vdd, vddio, foo, bar ]
---

<!-- {% assign supplies = "vdd, vddio" | split: ", " %} -->

# test-web
Just testing the GitHub features

## Include test

{% include quickstart.md %}

Include2 - foo:
{% include foo.md %}

Include3 - foo:
{% include foo3.md %}
