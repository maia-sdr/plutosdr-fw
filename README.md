# Maia SDR ADALM Pluto firmware

This repository contains the modified ADALM Pluto firmware for the
[Maia SDR](https://maia-sdr.org) project. See
[analogdevicesinc/plutosdr-fw](https://github.com/analogdevicesinc/plutosdr-fw)
for the default ADI firmware.

Latest binary Release : [![GitHub Release](https://img.shields.io/github/release/maia-sdr/plutosdr-fw.svg)](https://github.com/maia-sdr/plutosdr-fw/releases/latest)  [![Github Releases](https://img.shields.io/github/downloads/maia-sdr/plutosdr-fw/total.svg)](https://github.com/maia-sdr/plutosdr-fw/releases/latest)

Firmware License : [![Many Licenses](https://img.shields.io/badge/license-LGPL2+-blue.svg)](https://github.com/analogdevicesinc/plutosdr-fw/blob/master/LICENSE.md)  [![Many License](https://img.shields.io/badge/license-GPL2+-blue.svg)](https://github.com/analogdevicesinc/plutosdr-fw/blob/master/LICENSE.md)  [![Many License](https://img.shields.io/badge/license-BSD-blue.svg)](https://github.com/analogdevicesinc/plutosdr-fw/blob/master/LICENSE.md)  [![Many License](https://img.shields.io/badge/license-apache-blue.svg)](https://github.com/analogdevicesinc/plutosdr-fw/blob/master/LICENSE.md) and many others.

## Support

Support is handled through Github issues or dicussions. Issues dealing with the ADALM Pluto
firmware itself (building the firmware, flashing the firmware, etc.) should go
as
[issues in the plutosdr-fw repository](https://github.com/maia-sdr/plutosdr-fw/issues).
Issues having to do with Maia SDR (software or FPGA bugs, features requests, etc.)
should go as [issues in the maia-sdr repository](https://github.com/maia-sdr/maia-sdr/issues).
There are also
[Github discussions in the maia-sdr repository](https://github.com/maia-sdr/maia-sdr/discussions)
for any topics which are not issues (general questions, comments, etc.).

## Build instructions

Using the `ghcr.io/maia-sdr/maia-sdr-devel` Docker image from
[maia-sdr-docker](https://github.com/maia-sdr/maia-sdr-docker) is recommended to build
the firmware. To build the FPGA bitstream, Vivado 2021.2 is required.

Once the environment variables and `PATH` have been set as indicated in the
[Docker container README](https://github.com/maia-sdr/maia-sdr-docker#readme),
the firmware can be built using
```
make
```
 
## Pluto+

**Disclaimer:** The Maia SDR project acknowledges that the name Pluto+ is
  unfortunate, because this hardware device is unrelated to Analog Devices
  ADALM products. However, this device is not known by any other name, so us
  referring to it in another way would have been very confusing. Therefore,
  within Maia SDR, the firmware build for the Pluto+ is refered to as Pluto+ or
  `plutoplus`.

Here are some notes about the Pluto+ Maia SDR firmware.

The Pluto+ is largerly compatible with the ADALM-Pluto in terms of firmware. It
uses a different Zynq 7010 package and FPGA pinout, but its pinout ensures that
all the signals go to the same FPGA wirebonding pads (even though the BGA pins
are called differently and placed differently in the package). This means that a
regular ADALM-Pluto firmware mostly works on the Pluto+, though Ethernet and the
SD card will not work because the ADALM-Pluto does not have this hardware. There
is one pinout difference between the ADALM-Pluto and the Pluto+: the USB PHY
reset (URST) on the ADALM-Pluto is connected to MIO52. On the Pluto+ it is
usually connected to MIO46, because MIO52 is required for the Ethernet
MDIO. However, the Pluto+ has a jumper to allow connecting the USB PHY reset to
MIO52 instead when a firmware for the ADALM-Pluto (which does not support
Ethernet) is used (see the [plutoplus
README](https://github.com/plutoplus/plutoplus/tree/master#jumpers-and-pinouts)). When
using the Pluto+ Maia SDR firmware, it is required to connect the jumper to
MIO46.

There is usually no point in using the ADALM-Pluto Maia SDR firmware in a
Pluto+. Generally, the Pluto+ Maia SDR firmware should be used, as it supports
Ethernet and the SD card.

In order to distinguish it from the ADALM-Pluto firmware, the files for the
Pluto+ Maia SDR firmware are called `plutoplus` instead of `plutosdr` or
`pluto`. When using the USB storage firmware update method, the file that is
copied to the USB storage device must be called `pluto.frm`. The file
`plutoplus.frm` must be renamed to `pluto.frm`.

The
[`ipaddrmulti`](https://maia-sdr.org/installation/#configure-the-pluto-usb-ethernet)
feature can conflict with the IP address assignment for the Pluto+ Ethernet. It
is probably better to disable `ipaddrmulti` in the Pluto+.

The Pluto+ firmware can be built with
```
TARGET=plutoplus make
```
