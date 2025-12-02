* 抓包微信需要经常更新，而且获取数据变为越来越困难，我改用短信订阅的方式解决
* 订阅每天短信通知流量使用情况，没有语音数据
* iPhone快捷自动化处理短信，通过MQTT发送数据到HASS

      sensor:
        - name: "Data Left"
          icon: mdi:signal-5g
          state_topic: "unicom/state"
          unique_id: "Data_left"
          device:
            identifiers:
              - "5G"
            manufacturer: "Unicom"
            name: "Unicom"
          value_template: "{{ value_json.data_left }}"
          unit_of_measurement: "GB"
          state_class: measurement
          device_class: data_size

      
![unicom1](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Person/unicom1.png)
![unicom2](https://github.com/lifeexplore/Homeassistant-Project/blob/Homeassistant-Project/Dashboard/Person/unicom2.png)
