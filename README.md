概述

我从2024年初开始入坑Homeassistant，系统搭建已经相当完整。它即给我带来前所未有的方便，也带来非常多的乐趣。Hassbian在初期给了我非常多的帮助，各路大神帖子不仅给我各种新颖的方法，也为我的编程提供了很多的帮助。现在我的主要工具是Google，也用上了AI-Grok。我也希望能够回馈朋友们，希望我的总结能够为新手提供一定的帮助。

我的总结准备分以下的部分，具体说明了我的系统的构成，总结我的经验和教训。由于我的系统不可能覆盖不同类型的硬件，也不可能涵盖所有的功能和设置，完全基于我自身的需求考虑，水平有限，难免有很多的不足。仅供参考！

还有一点事先说明，我不分享UI的设计，如果有需要的伙伴，可以在Hassbian或者Bilibili上搜，有不少的大佬有很不错的分享，如：Frankiesmall, koryking等。
   1. [系统构成](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/System%20Composed.md)（网关的选择建议和说明）
   2. [集成列表](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/integrations.md)
   3. [仪表盘](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Layout.md)：日历，天气等基本功能设置
   4. [ESPHOME](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/README.md)：Picooc，青萍/小米温度计和Smart Light等BLE设备
   5. [Zigbee](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Zigbee.md)
   6. [围栏设置和人体监测](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Presence.md)
   7. TCP/IP网络设备，巧用EW11等
   8. MQTT：空调(climate)的实现，模式设置
   9. [读取HomePod传感器数据](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/README.md)
   10. HomePod，完美的音乐+语音控制+TTS
   11. 电视的组合设置（小米+Apple TV）
   12. NodeRed
   13. 杜亚窗帘485连接
   14. 电网数据
   15. 智能锁连接
   16. 12123数据跟踪
   17. 手机无线数据跟踪
   18. UIOT所谓Zigbee设备的替代
   19. 自动化一，Good Morning/Evening
   20. 自动化二，空调的不同模式，舒适/节能/睡觉
   21. 自动化三，电视的语音控制
   22. 自动化四，音乐播放睡眠定时
   23. 自动化五，警报的处理
   24. AI的使用
