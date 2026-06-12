说明：
* [C-Bus](https://www.se.com/tw/zh/product-subcategory/88010-cbus-家用自動化/)是施耐德公司旗下的一种基于微处理器的智能楼宇自动化系统，主要用于集成控制和管理建筑中的照明及电器设备
* 国内用的最多的是灯光的控制，[L5508RVF](https://www.se.com/hk/en/product/L5508RVF/relay-cbus-8-ch-10a-din-learn/)是最常用的控制器

方案：
* 首先实现C-Bus和计算机的连接，可以参考的[文档](https://cbus.readthedocs.io/_/downloads/en/latest/pdf/)和[方法](https://forums.whirlpool.net.au/archive/30x185k1)
* 硬件实现：[5500PC](https://www.cleverhome.com.au/manuals/Clipsal-C-Bus-5500PC-PC-Interface-Installation.pdf)+Elfin的[EW10](http://www.hi-flying.com/index.php?route=product/product/show&product_id=228)
* EW10的调试：https://blog.csdn.net/qq_44295125/article/details/107867234
* 连接设置：CNI，xx.xx.xx.xx:8899
* 施耐德的[Toolkit](https://www.se.com/au/en/download/document/C-Bus-Toolkit_V1160/)连接：https://www.schneider-electric.cn/zh/faqs/FA321883/
* Docker安装[cmqttd](https://github.com/micolous/cbus)，连接HASS
* HASS自动发现设备
	
补充：
* cmqttd会传输256个灯设备到HASS，如果不希望收到过多的垃圾，可以通过修改cmqttd.py和test_cmqttd.py减少数据发送