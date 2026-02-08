---
title: "watching ADS-B planes above you with a low cost @NooElec USB RTL-SDR"
date: 2019-12-26
categories: 
  - "fsse"
tags: 
  - "ads-b"
  - "aircraft"
  - "maps"
  - "rtl"
  - "sdr"
  - "usb"
---

watching planes above you with a USB RTL-SDR and and dump1090 or GNU Radio gr-air-modes

- [NooElec NE SDR SMArtee](https://amzn.to/2SqWj9q)
- https://blog.steve.fi/tracking\_aircraft\_in\_real\_time\_\_via\_software\_defined\_radio.html

installation process

- install virtualbox 6.x
- install virtualbox 6.x usb extensions
- install xubuntu 18
- run xubuntu vm

vi /etc/modprobe.d/blacklist-dvb-usb.conf and add the line

```
blacklist dvb_usb_rtl28xxu
```

install rtl-sdr

```
# aptitude install rtl-sdr
```

- connect RTL-SDR
- lsusb

run lsusb you should see

```
$ lsusb
Bus 001 Device 002: ID 0bda:2838 Realtek Semiconductor Corp. RTL2838 DVB-T
```

 

DUMP1090 howto

to get dump1090 to work you need to first install pkg-config and librtlsdr-dev

```
# aptitude install pkg-config librtlsdr-dev
```

then clone and make dump1090

```
$ git clone https://github.com/antirez/dump1090.git
$ cd dump1090
$ make
```

you can then run dump1090 and you should see something like

```
$ ./dump1090
Found 1 device(s):
0: Realtek, RTL2838UHIDIR, SN: 00000001 (currently selected)
Found Rafael Micro R820T tuner
Max available gain is: 49.60
Setting gain to: 49.60
Exact sample rate is: 2000000.052982 Hz
Gain reported by device: 49.60
*5d48825266c9cf;
CRC: 66c9cf (ok)
DF 11: All Call Reply.
  Capability  : Level 2+3+4 (DF0,4,5,11,20,21,24,code7 - is on airborne)
  ICAO Address: 488252

*02e1913021c8af;
CRC: 21c8af (ok)
DF 0: Short Air-Air Surveillance.
  Altitude       : 26600 feet
  ICAO Address   : 488252

*8d45d96958c912055dd13bf40ce4;
CRC: f40ce4 (ok)
DF 17: ADS-B message.
  Capability     : 5 (Level 2+3+4 (DF0,4,5,11,20,21,24,code7 - is on airborne))
  ICAO Address   : 45d969
  Extended Squitter  Type: 11
  Extended Squitter  Sub : 0
  Extended Squitter  Name: Airborne Position (Baro Altitude)
    F flag   : even
    T flag   : non-UTC
    Altitude : 39025 feet
    Latitude : 66222 (not decoded)
    Longitude: 119099 (not decoded)
```

exit with ^C

then run dump1090 --interactive --net to see an updating list of flights

```
$ ./dump1090 --interactive --net

Hex    Flight   Altitude  Speed   Lat       Lon       Track  Messages Seen   .
--------------------------------------------------------------------------------
400685 BAW65    7475      294     51.408    -0.051    97    1624      1 sec
394a05 AFR682   32000     523     51.435    0.409     315   499       17 sec
4ca302 RYR4BJ   21275     347     51.403    -0.396    167   1759      0 sec
45d969 VKG442   39025     431     51.427    -0.329    222   1746      0 sec
400efb EZY65AG  37000     425     51.486    -0.963    155   1215      1 sec
4064a1 TOM496   11450     315     51.222    -0.004    78    578       22 sec
45d963 VKG1502  32425     417     51.435    -0.614    218   2726      0 sec
398699 DJT100   34000     482     51.673    0.000     320   1481      1 sec
4ca9ea RYR993W  29000     404     51.469    0.315     101   4319      13 sec
4cc270 ICE6H    11700     313     51.237    -0.620    136   1800      27 sec
485873 KLM14N   33000     451     51.693    -0.156    74    3548      46 sec
```

 

or goto http://localhost:8080/ to see them plotted on a map

![Screenshot_2019-12-26 Screenshot](https://fsse8info.wordpress.com/wp-content/uploads/2019/12/screenshot_2019-12-26-screenshot.png)

![Screenshot_2019-12-26 Screenshot(1).png](https://fsse8info.wordpress.com/wp-content/uploads/2019/12/screenshot_2019-12-26-screenshot1.png)

GNU RADIO gr-air-modes howto

- https://www.rs-online.com/designspark/watching-planes-with-software-defined-radio
- https://www.gnuradio.org/
- https://github.com/bistromath/gr-air-modes
- https://github.com/gnuradio/pybombs
- https://www.cgran.org/
