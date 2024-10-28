!!! arduino
    This example assumes you are using the latest version of the Arduino IDE on your desktop. If this is your first time using the Arduino IDE, library, or board add-on, please review the following tutorials.

    - [Installing the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-arduino-ide)
    - [Installing Board Definitions in the Arduino IDE](https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide)
    - [Installing an Arduino Library](https://learn.sparkfun.com/tutorials/installing-an-arduino-library)

!!! note
    If you've never connected an CH340 device to your computer before, you may need to install drivers for the USB-to-serial converter. Check out our section on "[How to Install CH340 Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers)" for help with the installation.

    - [How to Install CH340 Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all)

SparkFun has written a library to work with the u-blox NEO-F10N. You can obtain this library through the Arduino Library Manager by searching for "**SparkFun u-blox GNSS v3**". Find the one written by SparkFun Electronics and install the latest version. Users who prefer to manually install the library can get it from the [GitHub Repository](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3) or download the .ZIP by clicking the button below:

<div style="text-align: center"><a href="https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3/archive/refs/heads/main.zip" class="md-button">SparkFun u-blox GNSS Arduino Library - v3 (ZIP)</a></div>

 Once you have the library installed checkout the various examples! There are several examples in the library that cover more than just the NEO-F10N. Note that some examples will not apply depending on the modules features. We will be looking at the [NEO-F10N folder](https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3/tree/main/examples/NEO-F10N).


!!! note
    According to the u-blox Integration Manual for the NEO-F10N, the current firmware does not support such as geofencing and low power mode so those examples contained in the library do not apply. Remember, the NEO-F10N only supports serial UART so the examples involving I<sup>2</sup>C and SPI do not apply either.
