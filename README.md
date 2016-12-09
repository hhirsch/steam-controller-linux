# Steam Controller
Instructions to run the steam controller under linux.

## Basic Setup
See comments in [70-steam-controller-permission.rule](./70-steam-controller-permission.rule) (1)

Tested on Manjaro 4.1.34-2

Fixed the following error for me:

    [ 751.559591] hid-generic 0003:2F00:1052.000F: usb_submit_urb(ctrl) failed: -1
    [ 751.559599] hid-generic 0003:2F00:1052.000F: timeout initializing reports
    [ 751.559722] hid-generic 0003:2F00:1052.000F: hiddev0,hidraw0: USB HID v1.11 Device [Valve Software BOOT LDR] on usb-0000:00:14.0-12.3/input0

## Steam Keyboard
In Order to get the Steam Keyboard to work make sure that the window "Steam Keyboard" is set to always on top undecorated and that it does not get the focus. (2)

- [steam-keyboard-mouse-focus.ds](./steam-keyboard-mouse-focus.ds) is a very unsatisfying fix (for awesomewm)
- [steam-keyboard.ds](./steam-keyboard.ds) is a fix for gnome

## Gamepad Emulation
Run the following command as root user:

    chown root:steamcontroller /dev/uinput; chmod g+rw /dev/uinput;
    
Tested on Manjaro 4.1.34-2

## What does not work?
- Gamepad emulation with steam games.

## Sources
1. https://wiki.archlinux.org/index.php/Gamepad#Steam_Controller
2. https://steamcommunity.com/app/353370/discussions/0/412449508278650766/
