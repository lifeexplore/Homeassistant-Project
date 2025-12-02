说明：
* 我的UIOT设备是交房自带的，功能简单可用，但是扩展性不好，兼容性极差，价格较高
* UIOT宣称基于Zigbee，其实它的设备只是传输层用的Zigbee（所谓的透传），协议层完全不兼容，完全无法用ZHA或者Z2Q链接，Z2T虽然可以链接，但也完全不能交换数据
* 针对不同的设备，我采取了不同的方案替代，效果很好，可以很稳定的运行

方案：
* 空调：我的空调是家用中央空调，UIOT通过IRACC控制器连接空调，再通过一个Zigbee的协议转换器和网关连接。这个转换器不稳定，有时会掉线，因此我完全摒弃了这个转换器。通过EW11实现网络的连接，NodeRed编程控制IRACC。具体请见：[空调](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/IRACC.md) 
* 传感器：Zigbee设备。由于网上没有任何的资料，我们只能想办法完全模拟UIOT的网关行为，连接它的Zigbee设备。
	1. [ZHA的连接效果](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/UIOT/ZHA.jpg)（Z2Q类似）
	2. Tasmato的连接效果
