# ESP-IDF Environment

### Install Home-brew
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
### Install pip
```
$ sudo easy_install pip
```
### Install Make & Ninjia
```
$ brew install make ninja dfu-util
```
### Clone ESP-IDF Repository
```
$ cd ~/Desktop
$ mkdir -p esp
$ cd esp
$ git clone --recursive https://github.com/espressif/esp-idf.git
```

### Install and setup ESP-IDF Environment
```
$ cd esp-idf
$ ./install.sh
$ . ./export.sh
```
```
$ cp -r $IDF_PATH/examples/get-started/hello_world ~/Desktop
$ cd ~/Desktop/hello_world/
```
## IDF Command
```
$ idf.py set-target esp32
$ idf.py menuconfig
$ idf.py build
```
### Find the Serial Port
```
$ ls /dev/tty.*
```
### Flash the firmware
```
$ idf.py -p /dev/tty.usbserial-********* -b 921600 flash
```
### Monitor
```
$ idf.py -p /dev/tty.usbserial-********* monitor
```

Note: the screen command would kll the usb serial connection, reconnect the ESP32 board when the screen command killed

### How to stop the idf monitor

```Ctrl + ]```

https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/tools/idf-monitor.html
