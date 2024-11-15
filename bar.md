---
#items:
configs:
  - config: CONFIG_MFD_ROHM_BD71828
    description: Enables the MFD core driver which handles interrupts and bus access. The core driver also launches the sub device drivers.
    subsystem: MFD
  - config: CONFIG_REGULATOR_BD71828
    description: Enables the regulator driver which provides control for individual regulatos.
    subsystem: regulator
  - config: CONFIG_COMMON_CLK_BD718XX
    description: Enables the clk driver which provides control for the clock gate
    subsystem: clk
  - config: CONFIG_GPIO_BD71828
    description: Enables the GPIO driver which provides control for the PMIC's generic purpose input/output pins.
    subsystem: GPIO
  - config: CONFIG_RTC_DRV_BD70528
    description: Enables the RTC driver which provides the control for the real time clock on PMIC. The RTC can maintain the time when SOC is turned off and provide timed events. Timed wake-up is also supported.
    subsystem: RTC

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

{% include kernel_configs.md %}

