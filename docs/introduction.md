


The [SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA](https://www.sparkfun.com/products/24114) is a standard precision GNSS board with meter-level positional accuracy. The NEO-F10N uses the L1/L5 bands instead of the more commonly seen L1/L2 bands. Utilizing the L5 band, the NEO-F10N delivers improved performance under challenging urban environments the L5 signals fall within the protected ARNS (aeronautical radio navigation service) frequency band. This band is less subject to RF interference.

<center>
<div class="grid cards" style="width:500px;" markdown>

-   <a href="https://www.sparkfun.com/products/24114">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/4/4/4/1/GPS-24114-NEO-F10N-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/24114">
      <b>SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA</b>
      <br />
      GPS-24114
      <br />
      <center>[Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/24114){ .md-button .md-button--primary }</center>
    </a>
</div>
</center>

<div style="text-align: center;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/lrZWDXNU0OE?si=9YpjbiSuIA6uKVQY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

This breakout supports concurrent reception of three GNSS constellations: GPS, Galileo, and BeiDou. The proprietary dual-band [multipath mitigation technology](https://www.u-blox.com/en/technologies/multipath-mitigation) from the u-blox F10 allows the module to choose the best signals from both bands to achieve a significantly better position accuracy in challenging urban environments than with the L1 band alone.

What's different from other u-blox modules is that the NEO-F10N module only supports one serial UART communication port. U-blox based GPS products are configurable using the popular, but dense, windows program called u-center. Plenty of different functions can be configured on the NEO-F10N: baud rates, update rates, spoofing detection, external interrupts, SBAS, etc. We've included a few basic UART examples with our SparkFun Arduino Library to get started.

In this tutorial, we'll go over the hardware and how to hookup the breakout board. We will also go over a few basic Arduino examples to get started!



### Required Materials

To follow along with this tutorial, you will need the following materials at a minimum. You may not need everything though depending on what you have. Add it to your cart, read through the guide, and adjust the cart as necessary.

* 1x [SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA [GPS-24114]](https://www.sparkfun.com/products/24114)
* 1x [Reversible USB A to C Cable - 0.8m [CAB-15425]](https://www.sparkfun.com/products/15425)
* 1x [Reinforced Interface Cable - SMA Male to TNC Male (10m) [CAB-21740]](https://www.sparkfun.com/products/21740)
* 1x [GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA) [GPS-23814]](https://www.sparkfun.com/products/23814)
* 1x [SparkFun IoT RedBoard - ESP32 Development Board [WRL-19177]](https://www.sparkfun.com/products/19177)


<div class="grid cards col-4" markdown>

<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/24114">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/4/4/4/1/GPS-24114-NEO-F10N-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/2322411488">
      <b>SparkFun GNSS L1/L5 Breakout - NEO-F10N, SMA</b>
      <br />
      GPS-24114
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/15425">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/3/9/8/4/15425-Reversible_USB_A_to_C_Cable_-_0.8m-02.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Reversible USB A to C Cable - 0.8m">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/15425">
      <b>Reversible USB A to C Cable - 0.8m</b>
      <br />
      CAB-15425
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/17519">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/6/5/9/3/17519-GPS_Antenna_Ground_Plate-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GPS Antenna Ground Plate">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/17519">
      <b>GPS Antenna Ground Plate</b>
      <br>
      GPS-17519
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/23814">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/4/1/3/8/23814-L1-L5-Multi-Band-High-Precision-GNSS-Antenna-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/23814">
      <b>GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA)</b>
      <br>
      GPS-23814
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/19177">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/8/8/0/0/ESP32_03.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun IoT RedBoard - ESP32 Development Board">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/19177">
      <b>SparkFun IoT RedBoard - ESP32 Development Board</b>
      <br />
      WRL-19177
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### GNSS Accessories

Depending on your setup, you may need the following mounting hardware. As included earlier in the required materials, the antenna ground plate below is needed when using multi-band antennas that do not have a good ground plane.

<!--
* 1x [GPS Antenna Ground Plate [GPS-17519]](https://www.sparkfun.com/products/17519)
* 1x [GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA) [GPS-23814]](https://www.sparkfun.com/products/23814)

-->

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/23814">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/4/1/3/8/23814-L1-L5-Multi-Band-High-Precision-GNSS-Antenna-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/23814">
      <b>GNSS L1/L5 Multi-Band High Precision Antenna - 5m (SMA)</b>
      <br>
      GPS-23814
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/17519">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/455-455/assets/parts/1/6/5/9/3/17519-GPS_Antenna_Ground_Plate-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GPS Antenna Ground Plate">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/17519">
      <b>GPS Antenna Ground Plate</b>
      <br>
      GPS-17519
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



For users that decide to use the SPK6618H multi-band antenna as an alternative, users would not need to include the antenna ground plate. The mounting hardware listed below is also typically used with the SPK6618H multi-band antennas. The reinforced interface cable between the SMA to TNC also needed for the SPK6618H multi-band antennas.

<!--
* [GNSS Magnetic Mount [PRT-21257]](https://www.sparkfun.com/products/21257)
* [GNSS Antenna Mounting Hardware Kit [KIT-22197]](https://www.sparkfun.com/products/22197)
* [Reinforced Interface Cable - SMA Male to TNC Male (10m) [CAB-21740]](https://www.sparkfun.com/products/21740)
* [GNSS Multi-Band L1/L2/L5 Surveying Antenna - TNC (SPK6618H) [GPS-21801]](https://www.sparkfun.com/products/21801)

-->

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/21801">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/2/1/5/9/7/SparkFun_GNSS_SPK6618H_Triband_Antenna_-_2-1.png" style="width:140px; height:140px; object-fit:contain;" alt="GNSS Multi-Band L1/L2/L5 Surveying Antenna - TNC (SPK6618H)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/21801">
      <b>GNSS Multi-Band L1/L2/L5 Surveying Antenna - TNC (SPK6618H)</b>
      <br />
      GPS-21801
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/21257">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/1/0/2/7/21257-_PRT_M90SD_Magnetic_Stand-_01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GNSS Magnetic Antenna Mount - 5/8" 11-TPI">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/21257">
      <b>GNSS Magnetic Antenna Mount - 5/8" 11-TPI</b>
      <br />
      TOL-21257
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/22197">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/2/0/9/7/22197-_01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="GNSS Antenna Mounting Hardware Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/22197">
      <b>GNSS Antenna Mounting Hardware Kit</b>
      <br />
      KIT-22197
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/21740">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/1/5/7/0/SparkFun_Reinforced_Interface_Cable_-_SMA_Male_to_TNC_Male_-_1.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Reinforced Interface Cable - SMA Male to TNC Male (10m)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/21740">
      <b>Reinforced Interface Cable - SMA Male to TNC Male (10m)</b>
      <br />
      CAB-21740
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->


</div>



### Radios &nbsp;_(Optional)_

For users that require radios to send data wirelessly, you could use the following radios.

<!--
* [SparkFun BlueSMiRF v2 - Headers](https://www.sparkfun.com/products/23287)
* [SiK Telemetry Radio V3 - 915MHz, 100mW [WRL-19032]](https://www.sparkfun.com/products/19032)
* [SparkFun LoRaSerial Kit - 915MHz (Enclosed) [WRL-20029]](https://www.sparkfun.com/products/20029)
-->

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/23287">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/3/4/8/3/23287-BlueSMiRF-ESP32-WithHeaders-Feature-NEW.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun BlueSMiRF v2 - Headers">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/23287">
      <b>SparkFun BlueSMiRF v2 - Headers</b>
      <br />
      WRL-23287
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/19032">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/8/6/3/4/19032-SiK_Telemetry_Radio_V3_-_915MHz__100mW-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SiK Telemetry Radio V3 - 915MHz, 100mW">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/19032">
      <b>SiK Telemetry Radio V3 - 915MHz, 100mW</b>
      <br />
      WRL-19032
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/20029">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/9/7/9/0/SparkFun_LoRaSerial_Enclosed_-_20029-1.jpg" style="width:140px; height:140px; object-fit:contain;" alt="SparkFun LoRaSerial Kit - 915MHz (Enclosed)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/20029">
      <b>SparkFun LoRaSerial Kit - 915MHz (Enclosed)</b>
      <br />
      WRL-20029
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->

</div>



### Tools &nbsp;_(Optional)_

You will need a soldering iron, solder, and [general soldering accessories](https://www.sparkfun.com/categories/49) for a secure connection when using the plated through holes. You will also need a hobby knife to disable the UART connection between the CH340 and the NEO-F10N.

<!--
* [PINECIL Soldering Iron Kit [TOL-24063]](https://www.sparkfun.com/products/24063)
* [Solder Lead Free - 15-gram Tube [TOL-9163]](https://www.sparkfun.com/products/9163)
* [Flush Cutters - Xcelite [TOL-14782]](https://www.sparkfun.com/products/14782)
* [Hook-Up Wire - Assortment (Stranded, 22 AWG) [PRT-11375]](https://www.sparkfun.com/products/11375)
* [Wire Stripper - 20-30 AWG Solid (22-32 AWG Stranded) [TOL-22263]](https://www.sparkfun.com/products/22263)
* [Hobby Knife [TOL-09200]](https://www.sparkfun.com/products/9200)
-->

<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/24063">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="PINECIL Soldering Iron Kit">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/24063">
      <b>PINECIL Soldering Iron Kit</b>
      <br />
      TOL-24063
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9163">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/2/5/8/7/09162-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Solder Lead Free - 15-gram Tube">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9163">
      <b>Solder Lead Free - 15-gram Tube</b>
      <br>
      TOL-09163
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11375">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hook-Up Wire - Assortment (Stranded, 22 AWG)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11375">
      <b>Hook-Up Wire - Assortment (Stranded, 22 AWG)</b>
      <br />
      PRT-11375
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/24771">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/3/9/4/7/24771-Wire-Strippers-Feature.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Wire Strippers - 20-30 AWG">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/24771">
      <b>Wire Strippers - 20-30 AWG</b>
      <br />
      TOL-24771
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/14782">
      <figure markdown>
        <img src="https://cdn.sparkfun.com//assets/parts/1/3/0/3/6/14782-Flush_Cutters_-_Xcelite-02.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Flush Cutters - Xcelite">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/14782">
      <b>Flush Cutters - Xcelite</b>
      <br />
      TOL-14782
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->

-   <a href="https://www.sparkfun.com/products/9200">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Hobby Knife">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9200">
      <b>Hobby Knife</b>
      <br />
      TOL-09200
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Prototyping Accessories &nbsp;_(Optional)_

For those using radios to connect a base station and rover together, you will need to connect to the PTHs. You could use IC hooks for a temporary connection depending on your setup and what you have available. Of course, you will want to the solder header pins for a secure connection. Below are a few prototyping accessories that you may want to consider.

<!--
* [Breadboard - Self-Adhesive (White) [PRT-12002]](https://www.sparkfun.com/products/12002)
* [IC Hook with Pigtail [CAB-09741]](https://www.sparkfun.com/products/9741)
* [Break Away Headers - Straight [PRT-00116]](https://www.sparkfun.com/products/116)
* [Female Headers [PRT-00115]](https://www.sparkfun.com/products/115)
* [Header - 6-pin Female (PTH, 0.1") [PRT-11894]](https://www.sparkfun.com/products/11894)
* [Jumper Wires Premium 6" M/M Pack of 10 [PRT-08431]](https://www.sparkfun.com/products/8431)
-->

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/12002">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/8/5/0/3/12002-Breadboard_-_Self-Adhesive__White_-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Breadboard - Self-Adhesive (White)">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/12002">
      <b>Breadboard - Self-Adhesive (White)</b>
      <br />
      PRT-12002
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/9741">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg" style="width:140px; height:140px; object-fit:contain;" alt="IC Hook with Pigtail">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/9741">
      <b>IC Hook with Pigtail</b>
      <br>
      CAB-09741
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/116">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/0/6/00116-02-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Break Away Headers - Straight">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/116">
      <b>Break Away Headers - Straight</b>
      <br />
      PRT-00116
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/115">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/0/5/00115-03-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Female Headers">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/115">
      <b>Female Headers</b>
      <br />
      PRT-00115
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/11894">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/parts/8/9/7/11894-02.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Header - 6-pin Female (PTH, 0.1")">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/11894">
      <b>Header - 6-pin Female (PTH, 0.1")</b>
      <br />
      PRT-11894
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
-   <a href="https://www.sparkfun.com/products/8431">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/1/1/8/1/JumperWire-Male-01-L.jpg" style="width:140px; height:140px; object-fit:contain;" alt="Jumper Wires Premium 6" M/M Pack of 10">
      </figure>
    </a>

    ---

    <a href="https://www.sparkfun.com/products/8431">
      <b>Jumper Wires Premium 6" M/M Pack of 10</b>
      <br />
      PRT-08431
    </a>
<!-- ----------WHITE SPACE BETWEEN PRODUCTS---------- -->
</div>



### Suggested Reading

If you aren’t familiar with the following concepts, we also recommend checking out a few of these tutorials before continuing.

<div class="grid cards col-4" markdown>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/9">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/parts/5/9/7/4/10890-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="GPS Basics">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/9">
      <b>GPS Basics</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/9/0/8/USB-to-serial_converter_CH340-closeup.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Install CH340 Drivers">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all">
      <b>How to Install CH340 Drivers</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/getting-started-with-u-center-for-u-blox">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/8/1/5/u-center.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Getting Started with U-Center for u-blox">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/getting-started-with-u-center-for-u-blox">
      <b>Getting Started with U-Center for u-blox</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-upgrade-firmware-of-a-u-blox-gnss-receiver">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/1/6/9/2/u-blox_firmware_upgrade_-_19.jpg" style="width:264px; height:148px; object-fit:contain;" alt="How to Upgrade Firmware of a u-blox GNSS Receiver">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-upgrade-firmware-of-a-u-blox-gnss-receiver">
      <b>How to Upgrade Firmware of a u-blox GNSS Receiver</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/serial-communication">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Serial Communication">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/serial-communication">
      <b>Serial Communication</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-work-with-jumper-pads-and-pcb-traces/introduction">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg" style="width:264px; height:148px; object-fit:contain;" alt="How to Work with Jumper Pads and PCB Traces">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-work-with-jumper-pads-and-pcb-traces/introduction">
      <b>How to Work with Jumper Pads and PCB Traces</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/5/Soldering_Action-01.jpg"style="width:264px; height:148px; object-fit:contain;" alt="How to Solder: Through-Hole Soldering">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering">
      <b>How to Solder: Through-Hole Soldering</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/arduinoThumb.jpg" style="width:264px; height:148px; object-fit:contain;" alt="Installing Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-arduino-ide">
      <b>Installing Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG" style="width:264px; height:148px; object-fit:contain;" alt="Installing Board Definitions in the Arduino IDE">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide">
      <b>Installing Board Definitions in the Arduino IDE</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
-   <a href="https://learn.sparkfun.com/tutorials/iot-redboard-esp32-development-board-hookup-guide">
      <figure markdown>
        <img src="https://cdn.sparkfun.com/assets/learn_tutorials/2/2/5/7/285808434_548438690244031_7008413248633042033_n.jpg"style="width:264px; height:148px; object-fit:contain;" alt="IoT RedBoard ESP32 Development Board Hookup Guide">
      </figure>
    </a>

    ---

    <a href="https://learn.sparkfun.com/tutorials/iot-redboard-esp32-development-board-hookup-guide">
      <b>IoT RedBoard ESP32 Development Board Hookup Guide</b>
    </a>
<!-- ----------WHITE SPACE BETWEEN GRID CARDS---------- -->
</div>

You may also be interested in the following blog posts on GNSS technologies.

<div class="grid cards col-4" markdown align="center">

-   <a href="https://www.sparkfun.com/news/4276">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/4/2/7/6/GPSvGNSSHomepageImage4.png)
	</figure>

	---

	**GPS vs GNSS**</a>
</div>
