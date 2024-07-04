# Wi-Fi Access Point Example

This example shows how to use the Wi-Fi Access Point functionality of the Wi-Fi driver of ESP32-S3 for serving as an Access Point.

### Configure the project

In the file `main/Kconfig.projbuild`:

* Set the Wi-Fi configuration.
    * Set `WiFi SSID`.
    * Set `WiFi Password`.

### Build and Flash

Build the project and flash it to the board, then run the monitor tool to view the serial output


## Example Output

There is the console output for this example:

```
I (530) phy_init: phy_version 670,b7bc9b9,Apr 30 2024,10:54:13
I (570) wifi:mode : softAP (cc:8d:a2:29:a1:79)
I (620) wifi:Total power save buffer number: 16
I (620) wifi:Init max length of beacon: 752/752
I (620) wifi:Init max length of beacon: 752/752
I (620) wifi Acess Point: wifi_init_softap finished. SSID:JOEJOEJOE password:spidermonkey channel:1
I (620) esp_netif_lwip: DHCP server started on interface WIFI_AP_DEF with IP: 192.168.4.1
I (640) main_task: Returned from app_main()
I (8500) wifi:new:<1,1>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (8500) wifi:station: 68:b6:b3:3d:5b:8c join, AID=1, bgn, 40U
I (8500) wifi:station: 68:b6:b3:3d:5b:8c leave, AID = 1, bss_flags is 232546, bss:0x3fca3314
I (8510) wifi:new:<1,0>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (11920) wifi:new:<1,1>, old:<1,0>, ap:<1,1>, sta:<255,255>, prof:1
I (11920) wifi:station: 68:b6:b3:3d:5b:8c join, AID=1, bgn, 40U
I (11940) wifi Acess Point: station 68:b6:b3:3d:5b:8c join, AID=1
I (11970) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.2
```
