
Now that we have our library and board add-on installed, we can start experimenting with the breakout board. For the scope of this tutorial, we will highlight one of the examples to get started. From there we will be able to build our own custom code to integrate the development board into a project.



### Example 1: NAV-SIG

This example shows how to configure the NEO-F10N GNSS for L5 band and overriding the health status. The output will indicate the type of signals that the NEO-F10N is receiving. Head to the example in the **NEO-10N** folder (located in **File** **Examples** > **SparkFun u-blox GNSS V3** > **NEO-F10N** > **Example1_NAV-SIG**).

If you have not already, select your Board (in this case the **SparkFun ESP32 IoT RedBoard**), and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. Give the NEO-F10N a few minutes to get a satellite lock. The signals available will be output in the Serial Monitor. If everything goes well, you should see some L5 signals (highlighted in red).

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/Arduino_NEO-F10N_IoT_RedBoard_ESP32_Output_Satellites_Highlighted.JPG"><img src="../assets/img/Arduino_NEO-F10N_IoT_RedBoard_ESP32_Output_Satellites_Highlighted.JPG" width="600px" height="600px" alt="NEO-F10N Signals and Health Status; L5 Highlighted"></a></td>
    </tr>
  </table>
</div>



### Example 12: Use UART

!!! note
    Make sure that you have the latest version of the SparkFun u-blox GNSS v3 Arduino Library when using the "Use UART" example. You will need a microcontroller (e.g. ESP32) with enough memory to compile this example.  Depending on the microcontroller that you use, you may also need to adjust the defined serial port from `Serial2` to `Serial1`.

This example shows how to output your coordinates and satellites in view through the Serial UART. Head to the example in the **NEO-10N** folder (located in **File** **Examples** > **SparkFun u-blox GNSS V3** > **Basics** > **Example12_UseUart**).

If you have not already, select your Board (in this case the **SparkFun ESP32 IoT RedBoard**), and associated COM port. Upload the code to the board and set the [Arduino Serial Monitor](https://learn.sparkfun.com/tutorials/terminal-basics/all#arduino-serial-monitor-windows-mac-linux) to **115200** baud. Once there are enough satellites in view you should be able to see your coordinates and the number of satellites in view!

<div style="text-align: center;">
  <table>
    <tr style="vertical-align:middle;">
     <td style="text-align: center; vertical-align: middle;"><a href="../assets/img/Arduino_NEO-F10N_IoT_RedBoard_ESP32_Output_Coordinates_SIV.JPG"><img src="../assets/img/Arduino_NEO-F10N_IoT_RedBoard_ESP32_Output_Coordinates_SIV.JPG" width="600px" height="600px" alt="Coordinates Shown in the Arduino Serial Monitor with the NEO-F10N "></a></td>
    </tr>
  </table>
</div>


### More Examples!

Now that you got it up and running, check out the SparkFun u-blox Arduino Library for other UART examples!

<div style="text-align: center"><a href="https://github.com/sparkfun/SparkFun_u-blox_GNSS_v3/tree/main/examples" target="github_gnss_v3" class="md-button">SparkFun_u-blox_GNSS_v3 > examples</a></div>
