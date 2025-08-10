主机：

* 硬件：AMDx86小主机，4网口，2USB，HDMI等
* OS：[OpenWrt](https://github.com/lifeexplore/OpenWrt-Setup)，[Docker](https://github.com/lifeexplore/OpenWrt-Setup/tree/OpenWrt-Setup/Docker/README.md) + [samba](https://github.com/lifeexplore/OpenWrt-Setup/tree/OpenWrt-Setup/Samba%20Setup/README.md) + [NetBird](https://github.com/lifeexplore/OpenWrt-Setup/tree/OpenWrt-Setup/NetBird%20Setup/README.md)
* 网络连接：[旁路由](https://github.com/lifeexplore/OpenWrt-Setup/README.md) + [OpenClash](https://github.com/lifeexplore/OpenClash-Auxiliary-Files/README.md)
* Docker容器：[NodeRed](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/NodeRed.md) + [ESPHome](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/ESPHome.md) + [Mosquitto](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/Mosquitto.md) + [Portainer](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/Portainer.md) + [HomeAssistant](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/Homeassistant.md) + [Calendar](https://github.com/lifeexplore/OpenWrt-Setup/blob/OpenWrt-Setup/Docker/Calendar.md)

Zigbee网关：

* 硬件：[藏机](https://www.zigbee.cc)
* 连接：Wifi
* OS：[Tasmota](https://tasmota.github.io/docs/)

BLE：

* 硬件：USB Dongle(淘宝¥20左右）
* 连接：USB
* OS：[ESPHome](https://esphome.io)

语音和音乐：

* 硬件：HomePod
* 连接：Wifi
* 音乐平台：苹果

电视：

* 硬件：小米 + Apple TV + HomePod
* 连接：HDMI(eARC)


说明：
1. 主机性能需要有一定的保障。不仅可以保证系统的响应，也为系统的功能扩充，软件安装留有一定的余量。
2. 上网一定要解决，否则软件的安装，以及资料的搜索都会有问题。
3. 建议一定要解决语言的问题，HASS是国外开发的软件平台，完全汉化不现实。
4. 多摸网关不建议使用，BLE和Zigbee会有干扰，带来稳定性问题。
5. 专用网关（如小米，涂鸦，SONOFF等）慎用。因为你需要完全依赖HACS中的集成来驱动，功能无法完全保证。
6. HomePod + Apple Music和HASS是最佳的组合，其它国内音箱的驱动都无法与之相比。
7. 没有BLE Mesh的使用经验。
