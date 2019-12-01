# autorotate

A simple script for automatic screen rotation, using a 3d acceleration sensor.

Configuration:
* Sensor name: Name of the acceleration sensor. Can usually be found at `/sys/bus/iio/devices/<device>/name`.
* Screen name: Name of the screen to rotate. Run `xrandr -q` to list all screens.
* Touch device ID: ID or name of the xf86-input-wacom touch device corresponding to the display. Run `xsetwacom --list devices` to list all devices.

The program handles SIGUSR1 to toggle rotation lock. This can be used to set up, for example, a keyboard shortcut to toggle rotation. The PID of the script can be found at `$XDG_RUNTIME_DIR/autorotate`, or, failing that, `/tmp/autorotate`.

Dependencies:
* python3
* xrandr
* pyudev
* pygobject
* gtk+3
