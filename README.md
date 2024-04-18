# BK7231 SPI Flasher
This is a simple SPI programmer for BK7231T chips. By default, everyone is using UART bootloader to program BK7231T, but in some rare cases one might overwrite Beken bootloader and thus brick the BK. The only way to unbrick it, is to use SPI flashing mode.

This tool is able to read and write whole flash content of BK7231T (maybe also other chips?) in the SPI mode, by using SPI access pins.

Tested only on Banana Pi, but should also work on Raspberry Pi.


## Getting started
### Raspberry Pi Zero W
- enable SPI in `raspi-config` (`sudo raspi-config nonint do_spi 0`)
- ensure rpi-gpio and python-dev package installed `sudo apt-get install python3-dev python3-rpi.gpio`
- create a self-contained python virtual environment: `python3 -m venv env` 
- active virtual environment: `source env/bin/activate`
- install `spidev` package: `python -m pip install spidev`

## BananaPi
- Use https://github.com/LeMaker/RPi.GPIO_BP instead of rpi-gpio


## Detailed writeup and guide:
https://www.elektroda.com/rtvforum/topic3931424.html
