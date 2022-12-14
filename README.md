![Action Shot](/images/OscilloscopeBoostbox.jpg)


[![YouTube Channel Views](https://img.shields.io/youtube/channel/views/UCz5BOU9J9pB_O0B8-rDjCWQ?label=YouTube&style=social)](https://www.youtube.com/channel/UCz5BOU9J9pB_O0B8-rDjCWQ)

[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/v_e_e_b/)

# Boostbox

Some notes on a command-line terminal, built from an old a super 8 viewer.

# Background

The Boostbox was originally a little project to turn an old Super 8 viewer into a YouTube viewing terminal. After some time tweaking it, it turned into a terminal that used tmux (multitasking), neomutt (email), weechat (IRC chat) and gcalcli (calendar) to spend as much time in a fast/responsive terminal as possible.

# Parts
- Raspberry Pi 4 or any single board computer running linux with HDMI out should work, for example a [Banana Pi M2 zero](https://www.veeb.ch/store/p/banana-pi-m2-zero) (disclaimer: we're selling these, so some of the price goes towards us buying coffee beans)
- Hanimex E300 super 8 viewer
- Ortholinear 40% keyboard
- AC to 5V DC power supply (to attach to power switch on Hanimex)
- 7inch 4:3 LED screen (like [this one](https://www.aliexpress.com/item/1005004454598585.html))
- Step-up convertor to convert 5V to the 9V DC needed by the screen
- Optional, a speaker that can fit in the recess that used to hold the bulb (alternatively, you can connect to an external speaker using bluetooth)

# Assembly

The shell is mostly empty, other than a bulb, a transformer, a lens and a plastic screen. These are easily removed (make sure you keep them in case you ever want to convert it back to a super 8 viewer).

Assembly will be influenced by the parts that you decide to use. One thing you are likely to need to do is to file away some metal to get the screen to fit. This part is tedious, but with the right tools (we used a simple metal file), it makes for a zen hour of crafting.

# Setup

Earlier iterations used Manjaro Linux (from the Raspberry Pi imager) but more recently, RaspiOS and Armbian was used. Use whatever you want.

The screen will be slightly obscured by the edges of the frame. This can be fixed by adding overscan values to `/boot/config.txt`.

For example:

```
overscan_left=40
overscan_right=10
overscan_top=40
overscan_bottom=16
```

# Software

A set of command line tools that with a bit of tenacity in remembering keyboard shortcuts, makes for an efficient workflow. In no particular order

## tmux

A terminal multiplexer
https://github.com/tmux/tmux/wiki

configuration: https://github.com/samoshkin/tmux-config

## neomutt

Old skool email

https://github.com/neomutt/neomutt

## gcalcli

Google calendar command line client

https://github.com/insanum/gcalcli

## weechat

IRC client

https://github.com/weechat/weechat

![Action Shot](/images/ircterminal.jpg)
## ytfzf

YouTube viewer

https://github.com/pystardust/ytfzf

# Video

[![Mod demo](http://img.youtube.com/vi/I5iHMEqll0Q/0.jpg)](http://www.youtube.com/watch?v=I5iHMEqll0Q "Video Title")


