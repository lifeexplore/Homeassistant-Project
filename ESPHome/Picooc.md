* 启发：https://lynx.st/posts/declouding-bluetooth-smart-scales
* APP发送数据：
  
      F1 09 3A 65 F7 4B A2 A5 00
      ^        ^           ^
      |        |           |
      | 头     | 时间戳      | 尾
  
* 接受的数据：

      39 0D 65 F7 4B A5 06 56 15 04 86 FC 00
      ^      ^          ^      ^
      |      |          |      |
      |头    |时间戳      |体重   | 阻抗
  
* 不同时间的产品有可能有区别，请自行抓包并修改程序
* 体重换算系数0.05
* 阻抗换算系数可以自行调整，0.125是比较了APP数据取的近似值
* [源码](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/ESPHome/esp32.yaml)
* 可以通过[小米体重秤](https://github.com/dckiller51/bodymiscale)获得进一步的数据，并且通过[卡片](https://github.com/dckiller51/lovelace-body-miscale-card?tab=readme-ov-file)输出[身体数据](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Person/Body.png)和[体重曲线](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Person/weight.png)
* 有一个问题请注意：小米体重秤的计算有bug，有时候算不出数据
