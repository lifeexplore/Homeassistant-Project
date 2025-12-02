![power](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Layout/power.jpg)

* 无论是国网还是南网，和联通一样，抓包越来越困难，而且水表和气表的数据也没有。所以我都转用快捷指令处理短信的方式每月更新数据。
* HASS[源码](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Layout/power.yaml) - [Apexcharts](https://github.com/RomRider/apexcharts-card)
* NodeRed获取数据，更新并且存储到文件，解决hass数据过期的问题，然后通过MQTT发给hass
