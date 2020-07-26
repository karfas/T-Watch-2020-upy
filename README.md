# T-Watch-2020-upy
Micropython on the TTGO T-Watch 2020

This are *very* early steps for the T-Watch 2020.

## Build micropython

I use the [pycopy](https://github.com/pfalcon/pycopy) fork of micropython, mostly for the async webserver we have here.

Requirements:
- esp-idf development system
```
git clone https://github.com/pfalcon/pycopy
git checkout v2.12.0.6    # due to Bug with mbedtls in v3

(cd pycopy/mpy-cross && make)
(cd pycopy/port/esp32 && make BOARD=GENERIC_SPIRAM)
(cd pycopy/port/esp32 && make deploy BOARD=GENERIC_SPIRAM PORT=/dev/ttyUSB0)

```
