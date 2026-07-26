## how to stop keyboard backlight timeout ubuntu

sudo find /sys/devices/ -name "*kbd_backlight"

- configure time out in secs

sudo nano <full path of kbd_backlight dir>/stop_timeout

change secs

ctrl + x, then Y (save) and Enter.



