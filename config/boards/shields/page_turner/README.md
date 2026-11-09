# Page Turner

Four-key BLE HID shield for a page-turner remote on nice!nano v2.

| Key | Binding     | Placeholder pin                        |
| --- | ----------- | -------------------------------------- |
| 1   | Page Up     | `P0.17` (Pro Micro D2, `&pro_micro 2`) |
| 2   | Page Down   | `P0.20` (Pro Micro D3, `&pro_micro 3`) |
| 3   | Volume Up   | `P0.22` (Pro Micro D4, `&pro_micro 4`) |
| 4   | Volume Down | `P0.24` (Pro Micro D5, `&pro_micro 5`) |

Switches are wired from the GPIO pin to ground. The pins are unused by the
nice!nano v2 board itself. `P0.17` and `P0.20` are the default I2C SDA/SCL
pinctrl pins while I2C is disabled; change `page_turner.overlay` if those
pins are needed for something else.

Current ZMK selects nice!nano v2 with board id `nice_nano//zmk` (revision
2.0.0 is the default). The old id `nice_nano_v2` was removed in the Zephyr
4.1 board migration.

GitHub Actions workflow `Build page-turner firmware` builds this shield and
uploads `page_turner-nice_nano_v2.uf2`. It does not flash a board.
