SparkFun GNSS L1/L5 Breakout- NEO-F10N, SMA
========================================

[![SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA](https://cdn.sparkfun.com/r/600-600/assets/parts/2/4/4/4/1/GPS-24114-NEO-F10N-Feature.jpg)](https://www.sparkfun.com/products/24114)

[*SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA (GPS-24114)*](https://www.sparkfun.com/products/24114)

The SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA is a standard precision GNSS board with meter-level positional accuracy. The NEO-F10N uses the L1/L5 bands instead of the more commonly seen L1/L2 bands. Utilizing the L5 band, the NEO-F10N delivers improved performance under challenging urban environments. The L5 signals fall within the protected ARNS (aeronautical radio navigation service) frequency band, leading to less RF interference.

This breakout supports the concurrent reception of three GNSS constellations: GPS, Galileo, and BeiDou. The proprietary dual-band multipath mitigation technology from the u-blox F10 allows the module to choose the best signals from both bands to achieve a significantly better position accuracy in challenging urban environments than with the L1 band alone.

What's different from other u-blox modules is that the NEO-F10N module only supports one serial UART communication port. We included a CH340 USB-to-serial converter to connect the board to a computer's USB port easily. For users connecting the board's serial UART pins to a microcontroller or radio, you will need to cut the USB-TX and USB-RX jumpers to avoid bus contention. Pins for power, serial, pulse per second, and control pins are broken out to 0.1"-spaced pins on the board's edge. We have also conveniently included a 1x6 header should you connect a BlueSMiRF v2 to transmit data wirelessly!

The breakout is also has an on-board rechargeable battery that provides power to the RTC on the NEO-F10N. This reduces the time-to-first fix from a cold start (~28s) to a hot start (2s). The battery will maintain RTC and GNSS orbit data without being connected to power for plenty of time. We have included an SMA connector for a secure connection.

U-blox-based GPS products are configurable using the popular but dense Windows program u-center. Plenty of different functions can be configured on the NEO-F10N: baud rates, update rates, spoofing detection, external interrupts, SBAS, etc. To get started, we've included a few basic UART examples with our SparkFun Arduino Library.

Repository Contents
-------------------
* **.github/workflows** - YAML files used for GitHub Actions and GitHub Pages/mkdocs
* **/Hardware** - KiCad design files (.brd, .sch)
  * **/Production** - Production panel files (.brd)
* **/docs** - Online documentation files
  * **/assets** - Folder containing all the file assets used for product documentation
    * **/3d_model** - Exported 3D models from KiCad
    * **/board_files** - Copy of design files used for product documentation
    * **/component_documentation** - Datasheets and manuals for hardware components
    * **/img** - Images for product documentation
  * **/github** - Files stating how to contribute and filing issues used for product documentation
  * **/javascript** - Folder containing custom javascript used for product documentation
  * **/stylesheet** - Folder containing CSS files used for product documentation
* **/overrides** - Customization files used for product documentation
  * **/.icons** - Icons used for GitHub used for product documentation
  * **./partials** - Used for product documentation

Documentation
--------------
* **[Library](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3)** - Arduino library for u-blox modules.
* **[Hookup Guide](https://docs.sparkfun.com/SparkFun_u-blox_NEO-F10N)** - Basic hookup guide for the NEO-F10N breakout board.

Product Versions
----------------
* [GPS-24114](https://www.sparkfun.com/products/24114) - Initial release

Version History
---------------
* v1.0 - Initial release

License Information
-------------------

This product is _**open source**_!

Please review the LICENSE.md file for license information.

If you have any questions or concerns on licensing, please contact technical support on our [SparkFun forums](https://forum.sparkfun.com/viewforum.php?f=152).

Distributed as-is; no warranty is given.

- Your friends at SparkFun.

_<COLLABORATION CREDIT>_
