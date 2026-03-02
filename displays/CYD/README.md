# ESP32cyd-2432s028
yaml code for esphome integration of a cheap 'yellow' display

More information can also be found here:
https://github.com/BOlaerts/ESP32-2432s028

Some basic info:
There are several components needed to make it work:
1. The display
2. The touchscreen
3. The backlight (because, nothing is shown when light isn't on. So in that case, the display could be functioning correctly, you just wouldn't be able to see it)

The display and touchscreen both use the SPI bus, so two different id's are needed.
The display is of type: ili9341 
The touchscreen is of type: xpt2046

LVGL is used to create the screens
