---
icon: sfe
---

!!! warning "Need Help?"
	If you need technical assistance or more information on a product that is not working as you expected, we recommend heading on over to the [SparkFun Technical Assistance](https://www.sparkfun.com/technical_assistanc) page for some initial troubleshooting.

	<article style="text-align: center;" markdown>
	[SparkFun Technical Assistance Page](https://www.sparkfun.com/technical_assistance){ .md-button .md-button--primary }
	</article>
	
	If you can't find what you need there, the [SparkFun Forums](https://forum.sparkfun.com/index.php) is a great place to search product forums and ask questions.
	
	!!! info "Account Registration Required"
		If this is your first visit to our forum, you'll need to create a [Forum Account](https://forum.sparkfun.com/ucp.php?mode=register) to post questions.



## Electrostatic Discharge
The mosaic-T module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.


!!! warning "ESD Precaution"
	As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.

	<div class="video-500px" style="text-align: center; margin: auto;" markdown>
	<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</div>



## USB Driver
A USB driver is only required for Windows PCs *(see the [USB Driver](software_overview.md#usb-driver) section)*.



## GNSS Antenna




### Power Input
!!! danger "Active Antenna"
	Never inject an external DC voltage into the SMA connector for the GNSS antenna, as it may damage the mosaic-T module. For instance, when using a splitter to distribute the antenna signal to several GNSS receivers, make sure that no more than one output of the splitter passes DC. Use [DC-blocks](https://en.wikipedia.org/wiki/DC_block) otherwise.



### Supported Frequency Bands
For the best performance, we recommend users choose a compatible L1/L2/L5 (tri-band) GNSS antenna and utilize a low-loss cable. Utilizing an antenna that doesn't match all the supported frequency bands of the mosaic-T, will result in reduced performance and capabilities.



## Data Logging
For data logging issues, here are some simple troubleshooting tips:

- Make sure that your SD card is formatted to a `FAT32` file system.
	- The `FAT32` file system also limits the maximum capacity of the card to less than **32GB** *(i.e. a 256GB SD card will not work)*.
- Make sure that the mosaic-T module has a configured data stream output.
- Use the mosaic-T web page to verify that the SD card is mounted as a storage drive.



## External Reference Clock
If the switch for an external reference clock is enabled, users must provide a 10MHz input signal. Otherwise, the mosaic-T module will cease to operate, without a clock signal. Additionally, switching between external and internal frequency reference must occur when the module is powered off, or the module must be reset after switching.
