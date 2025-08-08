简单方法：
  * 在ESPHome中打开Proxy + BLE Monitor扫描，在HASS添加设备
  * 在ESPHome中打开Proxy，并且设置Log为VERY_VERBOSE，在Log中获得信息

        [11:47:05][VV][esp32_ble_tracker:431]: Parse Result:
        [11:47:05][VV][esp32_ble_tracker:448]:   Address: xx:xx:xx:xx:xx:xx (PUBLIC)
        [11:47:05][VV][esp32_ble_tracker:450]:   RSSI: -83
        [11:47:05][VV][esp32_ble_tracker:451]:   Name: 'PICOOC-CQ'
        [11:47:05][VV][esp32_ble_tracker:459]:   Ad Flag: 6
        [11:47:05][VV][esp32_ble_tracker:462]:   Service UUID: 0xFFF0
        [11:47:05][VV][esp32_ble_tracker:474]:   Manufacturer ID: 0x000A, data: 75.57.05.0B.A3.1F (6)
        [11:47:05][VV][esp32_ble_tracker:483]:   Adv data: 02.01.06.03.03.F0.FF.09.FF.0A.00.75.57.05.0B.A3.1F.0A.09.50.49.43.4F.4F.43.2D.43.51.00 (29)

完整方法：
  * MAC + iOS: https://www.bluetooth.com/blog/a-new-way-to-debug-iosbluetooth-applications/


小米设备密码的获得：https://github.com/PiotrMachowski/Xiaomi-cloud-tokens-extractor
