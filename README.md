# ESP32 Freedom 

## Wifi Sniffer  (test build)

[original demo](https://github.com/lpodkalicki/blog/tree/master/esp32/016_wifi_sniffer)

[original blog post](https://blog.podkalicki.com/esp32-wifi-sniffer/)

### Build ESP32 Toolchain

```
curl https://raw.githubusercontent.com/lpodkalicki/blog/master/esp32/tools/build_esp32_toolchain.sh | bash -s -- -d ~/esp32

cd ~/esp32/esp-idf
./install.sh
```

You should see this:

```
Base directory: ~/esp32
ESP-Toolchain directory: ~/esp32/xtensa-esp32-elf/bin
ESP-IDF directory: ~/esp32/esp-idf
```

### Add export to bashrc

``` 
. $HOME/esp/esp-idf/export.sh
```

### Build and Run Sniffer

``` 
make menuconfig # linux users may not need this
make flash
```

### Connect via Serial

``` 
screen /dev/ttyUSB0 115200
```



## esp_wifi_80211_tx

[freedom output is deprecated](https://github.com/Jeija/esp32free80211). No [really](https://github.com/kieransimkin/esp8266-freedom).  [Hackaday article.](https://hackaday.com/2017/04/24/esp32s-freedom-output-lets-you-do-anything/)	

You want [this](https://github.com/espressif/esp-idf/blob/master/docs/en/api-guides/wifi.rst#wi-fi-80211-packet-send). Read [this](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/network/esp_wifi.html#_CPPv417esp_wifi_80211_tx16wifi_interface_tPKvib),

[original demo](https://github.com/Jeija/esp32-80211-tx)

### Build and Run Tx Demo

``` 
make menuconfig # linux users may not need this
make flash
```

### Connect via Serial

```
screen /dev/ttyUSB0 115200
```









## 







