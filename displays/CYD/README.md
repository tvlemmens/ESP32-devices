# ESP32cyd-2432s028
yaml code for esphome integration of a cheap 'yellow' display

More information can also be found here:
https://github.com/BOlaerts/ESP32-2432s028

Some useful links/libraries:
https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/tree/main?tab=readme-ov-file
https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/tree/main/Examples/ESPHome
https://www.xda-developers.com/cheap-yellow-display-addition-smart-home/
https://github.com/RyanEwen/esphome-lvgl/tree/main
https://www.youtube.com/watch?v=PsqMCoCTgTg


Some basic info:
There are several components needed to make it work:
1. The display
2. The touchscreen
3. The backlight (because, nothing is shown when light isn't on. So in that case, the display could be functioning correctly, you just wouldn't be able to see it)

The display and touchscreen both use the SPI bus, so two different id's are needed.
The display is of type: ili9341 
The touchscreen is of type: xpt2046

LVGL is used to create the screens


# ESP32-8048s050
Some ESPHome configs found (to be tested):
ESP32-8048S050 (Sunton 5.0” / CYD) Config - ESPHome - Home Assistant Community:
https://community.home-assistant.io/t/esp32-8048s050-sunton-5-0-cyd-config/782740
esphome-lvgl/devices/ESP32-8048S050.yaml at main · RyanEwen/esphome-lvgl:
https://github.com/RyanEwen/esphome-lvgl/blob/main/devices/ESP32-8048S050.yaml
agillis/esphome-configs: ESPHome config files for my devices:
https://github.com/RyanEwen/esphome-lvgl/blob/main/devices/ESP32-8048S050.yaml

## Working config:
https://github.com/RyanEwen/esphome-lvgl/blob/main/devices/ESP32-8048S050.yaml
### Note: Pixel frequency needs to be set to 15Mhz!
(iso 14Mhz as in the example config)


Hardware info:
5-inch 800x480 IPS TFT display - ST7262 (Parallel RGB-565 interface) (ST7262 seems to be recurring across sites)
Capacitive touch panel - GT911 (yet unclear if present on this board)
