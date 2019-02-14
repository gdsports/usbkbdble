# Convert USB keyboard to Bluetooth LE

![USB Keyboard to BLE converter](./images/usbkbdble.jpg)

## Hardware

* Adafruit Trinket M0
* USB OTG to host cable or adapter
* Adafruit nRF52840
* USB power bank, 5V out
* USB keyboard

Trinket M0	|nRF52840
------------|--------
GND			|GND
USB			|USB
TX (4)		|RX

## Software

### Trinket M0

Double click on the Trinket M0 reset.  When the TRINKETBOOT USB drive appears,
drag and drop the file KBDADVUARTUSBH.ino.trinket_m0.uf2 on the the drive.
This programs to the Trinket M0 to act as a USB host for the keyboard. USB
keyboard HID reports are send out the UART TX (4) pin. The source code is
at [https://github.com/gdsports/usbhostcopro](https://github.com/gdsports/usbhostcopro).

### Feather nRF52840

USBKBDBLE receives HID reports via its UART TX and sends the reports out the
BLE keyboard module.
