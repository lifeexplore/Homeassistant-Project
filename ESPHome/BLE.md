说明：
* BLE设备 - 廉价，部署方便(电池)
    * [ESPHome](https://esphome.io)：编程容易，扩展性很好
    * [ESP32](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/ESP32.png)：便宜，部署方便(USB/Wifi)
* ESPHome中的BLE：[BLE Gateway](https://github.com/myhomeiot/esphome-components#ble-gateway)，[BLE Monitor](https://custom-components.github.io/ble_monitor/Installation)
* [抓包BLE](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/sniff%20BLE.md) 
* [青萍传感器](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Rooms/Qingping.md)
* [小米温度/湿度传感器](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/LYWSD03.md)
* Smart Light灯具：https://github.com/aronsky/esphome-components
* Picooc电子秤
  
注意的问题：
* HASS可以直接访问BLE设备，但是实时性和编程性都不好，建议用ESPHome。如：青萍和小米的温度/湿度传感器
* 另外，分布控制可以减少程序的互扰，编程更加的清晰，可靠
* 下面中的type不建议用arduino，效率太低，内存占的很大，建议用esp-idf

      esp32:
        board: esp32dev
        framework:
          type: esp-idf
