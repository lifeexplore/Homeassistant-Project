* 微信获取数据变为不可能
* 订阅每天短信通知流量使用情况
* iPhone快捷程序处理短信，发送数据到HASS

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
