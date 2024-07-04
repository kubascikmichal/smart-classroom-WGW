# Wi-Fi Access Point Example UDP

This example shows how to use the Wi-Fi Access Point functionality of the Wi-Fi driver of the ESP32-S3 to serve as an Access Point and communicate with another device via the UDP protocol over IPv4.

### Configure the project

In the file `main/Kconfig.projbuild`:

* Set the Wi-Fi configuration.
    * Set `WiFi SSID`.
    * Set `WiFi Password`.
    * Set `UPD Port`

### Build and Flash

Build the project and flash it to the board, then run the monitor tool to view the serial output


## Example Output

There is the console output for this example when a device connected and sent some data:

```
I (574) UPD Server: wifi_init_softap finished. SSID:JOEJOEJOE password:spidermonkey channel:1
I (574) esp_netif_lwip: DHCP server started on interface WIFI_AP_DEF with IP: 192.168.4.1
I (594) UPD Server: Socket created
I (594) UPD Server: Socket bound, port 3333
I (604) UPD Server: Waiting for data
I (604) main_task: Returned from app_main()
I (1634) wifi:new:<1,1>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (1634) wifi:station: 68:b6:b3:3d:5b:8c join, AID=1, bgn, 40U
I (1654) UPD Server: station 68:b6:b3:3d:5b:8c join, AID=1
I (1684) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.2
I (2704) UPD Server: Received 111 bytes from 192.168.4.2:
I (2704) UPD Server: Temperature: 26.16, Humidity: 87.85, Lightness: 520.45, AQI: 47.56, GyroX: -71.55, GyroY: 18.30, GyroZ: -144.85
I (2714) UPD Server: Waiting for data
```

Device joined
```
I (1634) wifi:new:<1,1>, old:<1,1>, ap:<1,1>, sta:<255,255>, prof:1
I (1634) wifi:station: 68:b6:b3:3d:5b:8c join, AID=1, bgn, 40U
I (1654) UPD Server: station 68:b6:b3:3d:5b:8c join, AID=1
I (1684) esp_netif_lwip: DHCP server assigned IP to a client, IP is: 192.168.4.2
```

Server recieved some data from the client and send it back to it
```
I (2704) UPD Server: Received 111 bytes from 192.168.4.2:
I (2704) UPD Server: Temperature: 26.16, Humidity: 87.85, Lightness: 520.45, AQI: 47.56, GyroX: -71.55, GyroY: 18.30, GyroZ: -144.85
I (2714) UPD Server: Waiting for data
```
