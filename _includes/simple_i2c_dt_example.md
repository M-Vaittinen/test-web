### Devicetree example:

```
    i2c {
      #address-cells = <1>;
      #size-cells = <0>;
{%- if page.devicetype %}
      {{ page.devicetype }}@38 {
{%- else %}
      sensor@38 {
{%- endif %}
        compatible = {{ page.compatible }};
        reg = <0x38>;
{%- if page.dtsupply %}
    {%- for s in page.dtsupply %}
        {{ s }}-supply = <&{{ s }}>;
    {% endfor -%}
{%- endif %}
{%- if page.dtintparent %}
        interrupt-parent =  {{ page.dtintparent }};
{%- endif %}
{%- if page.dtints %}
        interrupts = {{ page.dtints }};
{%- endif %}
      };
    };
```

Where,

- "compatible" must be "{{ page.compatible }}" for the {{ page.sensorname }}.
- "reg" must be device's I2C address.
{%- if page.dtsupply %}
    {%- for s in page.dtsupply %}
- "{{ s }}-supply" refers to a regulator supplying "{{ s }}" power to the device.
    {%- endfor %}
{%- endif %}
{%- if page.dtintparent %}
- "interrupt-parent" refers to the interrupt controlled IRQ is wired to.
{%- endif %}
{%- if page.dtints %}
- "interrupts" specifies the pin in parent interrupt controller. See interrupt controller binding document for details.
{% endif %}
{% if page.bindinglink %}
See [the binding document]({{ page.bindinglink }}) for more information.
{% endif %}
