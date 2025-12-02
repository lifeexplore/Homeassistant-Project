![AC](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Rooms/AC.png)

* [Simple Thermostat](https://github.com/nervetattoo/simple-thermostat)卡片：preset实现空调的温度控制，节能效果明显
* 参考：https://bbs.hassbian.com/thread-8785-1-1.html
* IRACC控制器485连接[EW11](http://www.hi-flying.com/elfin-ew10-elfin-ew11)
* NodeRed控制
* [MQTT](https://www.home-assistant.io/integrations/climate.mqtt/)实现：部分HASS卡片[代码](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/AC%20card.yaml)，配置[代码](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/AC%20config.yaml)
* 空调带的温度计不准，尽量不要用。电子温度计也有一定的误差，需要相应调整
* 时长是历史运行时间，可以通过[历史数据](https://www.home-assistant.io/integrations/history_stats/)获得
