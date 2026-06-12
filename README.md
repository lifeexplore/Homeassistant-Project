概述

我从2024年初开始入坑Homeassistant，系统搭建已经相当完整。它即给我带来前所未有的方便，也带来非常多的乐趣。网上各路大神帖子给我很大的帮助，不仅见识了很多新颖的方法，也为我的编程提供了很多的帮助。现在我的主要工具是Google，也用上了AI-Grok。我也希望能够回馈朋友们，希望我的总结能够为新手提供一定的帮助。

我的总结准备分以下的部分，具体说明了我的系统的构成，总结我的经验和教训。由于我的系统不可能覆盖所有的不同类型硬件，也不可能涵盖所有的功能和设置，完全基于我自身的需求考虑，水平有限，难免有很多的不足。仅供参考！

我个人的原创包括：Picooc（有品）电子秤的驱动，UIOT设备接入。

值得参考的包括：Homekit生态及Homepod传感器读取，空调的节能控制，电视组合，AI的使用等。

还有一点事先说明，我不分享UI的设计，如果有需要的伙伴，可以在网上搜索，有不少的大佬有很不错的分享，如：Frankiesmall, koryking等。
   1. [系统构成](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/System%20Composed.md)：网关的选择建议和说明
   2. [集成列表](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/integrations.md)
   3. [仪表盘](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/README.md)：农历，天气等
   4. [空调的节能控制](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/IRACC.md)：可以从[费用曲线](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Layout/Expenses.png)中看到效果明显
   5. [BLE](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/README.md)：Picooc电子秤，青萍/小米温度计和Smart Light等
   6. [Zigbee](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Zigbee.md)：Tasmota方案
   7. [围栏设置和人体监测](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Presence.md)：iPhoneDetect
   8. [TCP/IP网络设备](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/TCP_IP.md)：EW11
   9. [MQTT](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/MQTT.md)：空调(climate)的实现/模式设置，窗帘(cover)控制
   10. [读取HomePod传感器数据](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/README.md)
   11. [HomeKit生态](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Homekit.md)：[Device](https://www.home-assistant.io/integrations/homekit_controller/) + [Bridge](https://www.home-assistant.io/integrations/homekit/)
   12. [电视组合](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Universal.md)：小米 + Apple TV
   13. [NodeRed](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/README.md)：空调，杜亚窗帘，日常费用，智能锁，12123数据追踪
   14. [自动化](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Automation.md)：早上/晚上问候，空调的不同模式，舒适/节能/睡觉，电视的语音控制，音乐播放睡眠定时，警报的处理
   15. [UIOT设备接入](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/UIOT/README.md)：空调/窗帘/传感器
   16. [C-Bus接入](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/CBUS/README.md)：灯光
   17. [远程控制](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/remote.md)：Tailscale
   18. [AI的使用](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/gemini.md)：Gemini
