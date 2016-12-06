# Steam Controller
Instructions to run the steam controller under linux.

Tested on Manjaro 4.1.34-2

Fixed the following error for me:

    [ 751.559591] hid-generic 0003:2F00:1052.000F: usb_submit_urb(ctrl) failed: -1
    [ 751.559599] hid-generic 0003:2F00:1052.000F: timeout initializing reports
    [ 751.559722] hid-generic 0003:2F00:1052.000F: hiddev0,hidraw0: USB HID v1.11 Device [Valve Software BOOT LDR] on usb-0000:00:14.0-12.3/input0

## Sources
- https://wiki.archlinux.org/index.php/Gamepad#Steam_Controller
