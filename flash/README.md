# Basic Flashing Sequence

## Flashing USBaspLoader

1. Connect ISP pins on board to ISP programmer
2. Use `make check` to ensure a proper connection
3. When proper connection is ensured, use `make fuse` to set fuses
4. After fuses are set, use `make flash` flash USBaspLoader

The relevant hex file is `main.hex`, which was compiled using a modified version
of
[USBaspLoader-Atmega32](https://github.com/khairulhasanmd/USBaspLoader-Atmega32)
that takes into account the settings found in
[`bootloaderconfig.h`](bootloaderconfig.h).

## Flashing QMK

1. Connect device to computer via USB port
2. Short bootloader jumper on device and press the reset switch
3. If done properly, the board should be recognized as a USB device
4. Flash QMK with `make upload`

The relevant hex file is `andyboard_default.hex`, which was compiled using a
modified version of [QMK](../qmk_firmware).

