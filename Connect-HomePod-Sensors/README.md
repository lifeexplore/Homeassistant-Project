目的：将HomePod的温度和湿度传感器数据实时传入HomeAssistant

WARNING！
* IOS27开始，苹果封锁了Homepod和Apple TV的URL访问权限，此方法失效！
* 解决方法：
	1. 用Apple TV HD（第四代，之前的版本没有测试过），TVOS26.6，将家庭中枢指向它。
	2. 用在家的iPad快捷指令（URL可以运行）。

需要的平台：
  1. HomeAssistant
  2. IOS需要27以下
	
原理：
  1. 由于IOS的不开放，不可能从其它的软件访问IOS内部的数据，也不可能直接放访问HomePod获得数据，因此只能定时由IOS将数据送给HomeAssistant。
  2. 分工：
	a. 传感器在HomeAssistant下定义；
	b. 由于Homekit不能定时触发事件，HomeAssistant提供Homekit Bridge定时触发Homekit的自动化进程；
	c. Homekit将传感器的数据送到HomeAsssitant的实体中。
		
主要的参考：
  https://community.home-assistant.io/t/how-to-integrate-homepod-mini-sensors-into-home-assistant-when-direct-integration-isnt-possible/665074/134
		    
步骤：
  1. 在configuration.yaml中增加定义[boolean](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/boolean.yaml)
  2. 通过Homekit Bridge将boolean传递给[Boolean-in-HomeKit](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/Boolean-in-HomeKit%20.png)
  3. [定义传感器](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/sensor.yaml)
  4. 设置HomeAssitant下的自动化：[timer_to_homekit](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/timer_to_homekit.yaml)
  5. 从HomeAssistant获取授权的长效Token
  4. 设置Homekit的自动化进程：[automation_1](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/Automation_1.jpg)，[automation_2](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/Automation_2.jpg)，[automation_3](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/Automation_3.jpg)，[automation_4](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Connect-HomePod-Sensors/Automation_4.jpg)
     
Homekit设置说明：
  1. HomeKit Bridge设置的Boolean为触发器
  2. 在Home App下的自动化直接编程，不需要单独的捷径，这样iPhone不参与数据的更新
  3. 获得的数据类型可以选择，需要选择为数字类型，这样可以统计，追寻历史
  4. POST的头设置：Authorization，Bearer xxxxxxxxxxxxxxxx(HomeAssistant的token)
