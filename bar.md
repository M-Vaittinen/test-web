---
#items:
configs:
  - config: CONFIG_MFD_ROHM_BD71828
    subsystem: mfd
  - config: CONFIG_REGULATOR_BD71828
    description: Enables the regulator driver which provides control for individual regulatos.
    subsystem: regulator
  - config: CONFIG_COMMON_CLK_BD718XX
    description: Enables the clk driver which provides control for the clock gate
    subsystem: clk
  - config: CONFIG_GPIO_BD71828
    description: Enables the GPIO driver which provides control for the PMIC's generic purpose input/output pins.
    subsystem: gpio
  - config: CONFIG_RTC_DRV_BD70528
    description: Enables the RTC driver which provides the control for the real time clock on PMIC. The RTC can maintain the time when SOC is turned off and provide timed events. Timed wake-up is also supported.
    subsystem: rtc
  - config: CONFIG_I_JUST_INVENTED_THIS_FOR_TESTING_NO_DESCRIPTION
    subsystem: watchdog
---

{% include kernel_conf_tbl.md %}

