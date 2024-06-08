Serial installation

Some rough notes

```
/data/conf/serial-starter.d# cat aec.conf 

service aec dbus-aec-serial


udevadm info /dev/ttyACM0

/etc/udev/rules.d/serial-starter.rules

add

ACTION=="add", ENV{ID_BUS}=="usb", ENV{ID_SERIAL_SHORT}=="5434025891",            ENV{VE_SERVICE}="aec"

udevadm trigger /dev/ttyACM0
```
