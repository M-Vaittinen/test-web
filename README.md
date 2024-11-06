---
permalink: /
model: my-model
flag: my-flag
test.rss1: res1
test.rss2: res2
---

{% assign supplies = "vdd, vddio" | split: ", " %}

# test-web
Just testing the GitHub features

## Include test

{% include quickstart.md %}

Include2 - foo:
{% include foo.md %}

Include3 - foo:
{% include foo3.md %}
