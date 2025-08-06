概述

我从2024年初开始入坑Homeassistant，系统搭建已经相当完整。它即给我带来前所未有的方便，也带来非常多的乐趣。Hassbian在初期给了我非常多的帮助，各路大神帖子不仅给我各种新颖的方法，也为我的编程提供了很多的帮助。现在我的主要工具是Google，也用上了AI-Grok。我也希望能够回馈朋友们，希望我的总结能够为新手提供一定的帮助。

我的总结准备分以下的部分，具体说明了我的系统的构成，总结我的经验和教训。由于我的系统不可能覆盖不同类型的硬件，也不可能涵盖所有的功能和设置，完全基于我自身的需求考虑，水平有限，难免有很多的不足。仅供参考！

还有一点事先说明，我不分享UI的设计，如果有需要的伙伴，可以在Hassbian或者Bilibili上搜，有不少的大佬有很不错的分享，如：Frankiesmall, koryking等。
   1. [系统构成](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/System%20Composed.md)（网关的选择建议和说明）
   2. 界面设计，日历，天气等基本功能设置
   3. ESPHOME，Picooc，小米温度计和落地灯等BLE设备
   4. Zigbee，Z2M/ZHA/Z2T的选择
   5. TCP/IP网络设备，巧用EW11等
   6. NodeRed
   7. 为什么要用MQTT？
   8. 围栏设置和人体监测
   9. [读取HomePod传感器数据](https://github.com/lifeexplore/Homeassistant-Project/tree/Homeassistant-Project/Connect-HomePod-Sensors)
   10. HomePod，完美的音乐+语音控制+TTS
   11. 电视，和Apple TV的完美组合
   12. UIOT所谓Zigbee设备的替代
   13. 电子秤连接
   14. 空调的MQTT实现，模式设置
   15. 电视的组合设置（小米+Apple TV）
   16. 杜亚窗帘485连接
   17. 电网数据
   18. 智能锁连接
   19. 12123数据跟踪
   20. 摄像头连接
   21. 手机无线数据跟踪
   22. 自动化一，Good Morning/Evening
   23. 自动化二，空调的不同模式，舒适/节能/睡觉
   24. 自动化三，电视的语音控制
   25. 自动化四，音乐播放睡眠定时
   26. 自动化五，警报的处理
