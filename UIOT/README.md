说明：
* 我的UIOT设备是交房自带的，功能简单可用，但是扩展性不好，兼容性极差，价格较高
* UIOT宣称基于Zigbee，其实它的设备只是传输层用的Zigbee（所谓的透传），协议层完全不兼容，完全无法用ZHA或者Z2Q链接，Z2T虽然可以链接，但也完全不能交换数据
* 针对不同的设备，我采取了不同的方案替代，效果很好，可以很稳定的运行

方案：
* 空调：我的空调是家用中央空调，UIOT通过IRACC控制器连接空调，再通过一个Zigbee的协议转换器和网关连接。这个转换器不稳定，有时会掉线，因此我完全摒弃了这个转换器。通过EW11实现网络的连接，NodeRed编程控制IRACC。具体请见：[空调](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/NodeRed/IRACC.md) 
* 传感器：Zigbee设备。由于网上没有任何的资料，我们只能想办法完全模拟UIOT的网关行为，连接它的Zigbee设备。
	1. [ZHA的连接效果](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/UIOT/ZHA.jpg)（Z2Q类似）
	2. [Tasmato的连接效果](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/UIOT/Tasmota.jpg)：可以看到6A0有数据出错，但很快输出"FF23890001AB"后脱机
	3. [抓包](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/UIOT/first.jpg)：通过数据类型41输出
	4. 分析结果：
		a. 设备和网关通过6A0交换数据，数据类型41
		b. 入网后，设备首先发送"FF238BFFFFFFFFA8"，然后发送"FF238000158D00041EA4EE000021310419031404196C"，如果没有应答，或者回答错误，进入休眠模式
		c. 第一个数据需要回答"FF238BFFFFFFFFA4"，如果回答不对，网关只能收到不完整数据"FF238000158D00041EA4EE0000213104190317B"
		d. 第二个数据需要回复"FF238000158D00041EA4EE000021310419031411B7D7"
	5. 方案实现：结果反复试验，分析，终于成功！！
		a. Zb文件 - 所有UIOT设备
			#Z2Tv1
			# UIOT payload type 
			:UIOT*,
			06A0/0001,CustomData		
		b. Rule 2 - 第一个参数
			Rule2
      			on ZbReceived#CustomData=FF238BFFFFFFFFA8 do ZbSend {"Device":%zbdevice%,"Send":"06a0_0a/01004108ff238b030c0300a4"} endon
    		Rule2 1		
		c. Rule 3
			Rule3
      			on ZbReceived#CustomData=FF238000158D00041EA4EE000021310419031404196C do ZbSend {"Device":%zbdevice%,"Send":"06A0_0a/01004116ff238000158d00041ea4ee000021310419031411b7d7"} endon
      		Rule3 1