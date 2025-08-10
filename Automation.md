HASS的自动化：
* 可编程性很强：触发条件极丰富，嵌套可以很复杂
* 编写方便：可视或者YAML，可跟踪
* 脚本功能强大：可调用，嵌套

早上/晚上问候：
* 定义二元开关，映射到Home
* 特定条件触发，TTS问候，然后打开二元开关，触发Home中的自动化，播放指定的音乐

空调模式控制：
* 不同的时段，通过空调的Preset，设定舒适/清凉/睡觉等模式
* 空调自动运行在设定的温度范围内，降低能耗([电量曲线](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Layout/power.jpg)），提高效率
* 也可以通过HomePod的语音触发

电视的语音控制
* 音乐播放睡眠定时
* 警报的处理
