# autorotate

A simple script for automatic screen rotation, using a 3d acceleration sensor. Requires root.

Configuration:
* sensorname: Name of the acceleration sensor. Can usualy be found at `/sys/bus/iio/devices/<device>/name`.
* screenname: Name of the screen to rotate. Run `xrandr -q` to list all screens.
* rotLockKey: Keystroke to disable rotation. See [here](https://github.com/boppreh/keyboard) for acceptable options.
* touchID: ID of the xf86-input-wacom touch device corresponding to the display. Run `xsetwacom --list devices` to list all devices.

Dependencies:
* python3
* xrandr
* pyudev
* pygobject
* keyboard
* gtk+3
* AppIndicator (optional)
