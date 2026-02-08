---
title: "RTL SDR with luaradio"
date: 2019-12-26
categories: 
  - "fsse"
tags: 
  - "lua"
  - "luaradio"
  - "rtl"
  - "sdr"
---

RTL SDR with luaradio

- [NooElec NE SDR SMArtee](https://amzn.to/2SqWj9q)
- https://hackaday.com/2019/12/24/luaradio-gives-insight-into-sdr/
- https://github.com/vsergeev/luaradio

pre install

```
# aptitude upgrade pulseaudio
# aptitude install libpulse-dev
# aptitude install luajit libluajit-5.1-dev
```

build luaradio

```
$ git clone https://github.com/vsergeev/luaradio.git
$ cd luaradio 
$ cd embed
$ make
$ sudo make install
$ cd ..
```

run luaradio to listen to Smooth FM

```
$ luaradio examples/rtlsdr_wbfm_mono.lua 102.2e6
```

the luaradio lua code to listen to Smooth FM

```
-- Blocks
local source = radio.RtlSdrSource(frequency + tune_offset, 1102500)
local tuner = radio.TunerBlock(tune_offset, 200e3, 5)
local fm_demod = radio.FrequencyDiscriminatorBlock(1.25)
local af_filter = radio.LowpassFilterBlock(128, 15e3)
local af_deemphasis = radio.FMDeemphasisFilterBlock(75e-6)
local af_downsampler = radio.DownsamplerBlock(5)
local sink = radio.PulseAudioSink(1)

-- Connections
local top = radio.CompositeBlock()
top:connect(source, tuner, fm_demod, af_filter, af_deemphasis, af_downsampler, sink)
top:run()
```
