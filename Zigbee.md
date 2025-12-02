方案选择：Tasmota
* [Zigbee2MQTT](https://www.zigbee2mqtt.io)：Docker安装，支持设备较多，可编程性一般，控制较困难
* [ZHA](https://www.home-assistant.io/integrations/zha/)：HASS直接控制，支持设备较少，可编程性一般
* [Zigbee2Tasmota](https://tasmota.github.io/docs/)：独立运行，支持设备有限，但可编程性很好

网关：[藏机](https://www.zigbee.cc)

设备：
* 人体存在传感器 - [SNZB-06P](https://support.sonoff.tech/zh-hans/snzb-06p-usermanual/)
* 温湿度传感器 - [TS0601](https://www.zigbee2mqtt.io/devices/TS0601_temperature_humidity_sensor_1.html)

特点：
* 响应较快
* 数据更新及时
* 成本高于BLE
* 对比BLE Mesh没有经验

抓包：Wireshark
* 参考：https://e2echina.ti.com/support/wireless-connectivity/zigbee-and-thread/f/zigbee-thread-forum/162782/wireshark-zigbee-sniffer
* 硬件：Windows + USB Dongle
