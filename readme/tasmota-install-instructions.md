# Tasmota Install Instructions

Upload Tasmota Client Firmware on to the NodeMCU. The firmware .bin file is available on Moodle.

Steps:

1. Using the ESPTool utility (available on Moodle), from the command line Erase NodeMCU — `esptool.exe --port COM5 erase_flash`(_**change the COM port to whichever matches your board’s port )**_.
2. Using the ESPTool utility, from the command line upload the Tasmota firmware — `esptool.exe --port COM5 write_flash -fs 1MB -fm dout 0x0 tasmota.bin` (_**change the COM port to whichever matches your board’s port ).**_
3. When the NodeMCU reboots it should act as a WiFi Access Point (hotspot) with an SSID of t_**asmota-xxx-xxxx**_
4. Once connected open your web browser to [**http://192.168.4.1**](http://192.168.4.1), you will be presented with the Tasmota WiFi configuration page. Enter the SSID and password for your WiFi Access Point. The NodeMCU will give you an IP address that it can be reached at (e.g 10.100.1.10), note this IP address. Connect your PC back to the same network that you have set in the Tasmota WiFi set up and connect to the NodeMCU by pointing your web browser to the IP address you noted.
5. Reconnect your PC back to the same network that you have set in the Tasmota WiFi set up and connect to the NodeMCU by pointing your web browser to the IP address you noted in step 4.
6. You will now be presented with Tasmota’s main page. Click on **Configuration**.
7. In the next menu click on **Configure Module**
8. Now set the **Module type** to **Generic** (the NodeMCU will reboot) and then map the pins for your NodeMCU as shown below.
9. Finally configure the MQTT broker you will be using (the Mosquito server on Azure)
