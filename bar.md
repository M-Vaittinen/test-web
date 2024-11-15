---
#items:
configs:
  config_foo: Foo is for bazzing
  config_bar: Bar is not for fuzzing
  config_baz: Can be for anything

conf:
  - config: CONFIG_FOO_MFD
    description: Enables FOO
    subsystem: MFD
  - config: CONFIG_FOO_CLK
    description: Enables BAR
    subsystem: CLK
  - config: CONFIG_FOO_GPIO
    description: Enables BAZ
    subsystem: GPIO
---

{% include arr.md %}

{% include obj.md %}

