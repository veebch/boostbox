![Action Shot](/images/OscilloscopeBoostbox.jpg)

[![YouTube Channel Views](https://img.shields.io/youtube/channel/views/UCz5BOU9J9pB_O0B8-rDjCWQ?style=flat&logo=youtube&logoColor=red&labelColor=white&color=ffed53)](https://www.youtube.com/channel/UCz5BOU9J9pB_O0B8-rDjCWQ) [![Instagram](https://img.shields.io/github/stars/veebch?style=flat&logo=github&logoColor=black&labelColor=white&color=ffed53)](https://www.instagram.com/v_e_e_b/)


# Boostbox

Some notes on a command-line terminal, (reversibly) built into an old a super 8 film viewer. The aim is to make a functional terminal rather than just bunging an SBC into something old and it looking cool.


# Background

The Boostbox was originally a little project to turn an old Super 8 viewer into a YouTube viewing terminal. After a year or so of tweaking it, it turned into a capable terminal that does: 
- terminal mutiplexing (tmux)
- email (neomutt) 
- encryption (pgp)
- GTD (taskwarrior)
- chat (weechat)
- video/ image viewing (the small screen isn't brilliant for it)
- audio (bluetooth and ncmcpp and mpd)

# Overview Video

Click/tap the image below for a walk through of the build.


[![Explainer video](http://img.youtube.com/vi/I5iHMEqll0Q/0.jpg)](http://www.youtube.com/watch?v=I5iHMEqll0Q "Video Title")


# Parts
- Raspberry Pi 4 or any single board computer running linux with HDMI out should work
- Hanimex E300 super 8 viewer
- AC to 5V DC power supply (to attach to power switch on Hanimex)
- 7inch 4:3 LED screen (like [this CLAA070MA0ACW](https://www.aliexpress.com/item/1005004454598585.html)) (Dimensions 154 × 119,2 × 5,4)
- Step-up convertor to convert 5V to the 9V DC needed by the screen (we used an adjustable MT3608 DC-DC convertor)
- Optional, a speaker that can fit in the recess that used to hold the bulb (alternatively, you can connect to an external speaker using bluetooth)
- A [BM40 keyboard](https://kprepublic.com/products/bm40-rgb-40-hot-swap-custom-mechanical-keyboard-pcb-qmk-underglow-type-c-planck?variant=40660715536547) by kprepublic. Layers set up using [QMK](https://github.com/qmk/qmk_firmware) to add mouse-emulation keys for those surprisingly rare moments that call for a mouse.
# Assembly

The shell is mostly empty, other than a bulb, a transformer, a lens and a plastic screen. These are easily removed (make sure you keep them in case you ever want to convert it back to a super 8 viewer).

Assembly will be influenced by the parts that you decide to use. One thing you are likely to need to do is to file away some metal to get the screen to fit. This part is tedious, but with the right tools (we used a simple metal file), it makes for a zen (long, boring) hour of crafting.

# Setup

Earlier iterations used Manjaro Linux (from the Raspberry Pi imager) but more recently vanilla RaspiOS was used and everything was done in a the framebuffer-enabled console. 

The screen will be slightly obscured by the edges of the frame. This can be fixed by adding overscan values to `/boot/config.txt`.

For example:

```
overscan_left=40
overscan_right=10
overscan_top=40
overscan_bottom=16
```

# UX / Tools

An evolving set of command line tools that make for an efficient workflow. Some things to make them a little easier to navigate are in the [cheat-sheets directory](./cheatsheets).

In no particular order:

### Terminal multiplexer

- [tmux](https://github.com/tmux/tmux/wiki) with [configuration](https://github.com/samoshkin/tmux-config) by @samoshkin.
- Start up elaborate sessions using a single [tmuxinator](https://github.com/tmuxinator/tmuxinator) command.

### Email

- [neomutt](https://github.com/neomutt/neomutt), a fast, flexible email client.

### Encryption

- GNU Privacy Guard [GPG](https://gnupg.org/).

### Calendar

- Google calendar command line client [gcalcli](https://github.com/insanum/gcalcli).

### Chat

-  IRC client, [weechat](https://github.com/weechat/weechat).

### GTD

- Getting Things Done™, [Task Warrior](https://github.com/GothenburgBitFactory/taskwarrior)

### Video and Audio

- [ytfzf](https://github.com/pystardust/ytfzf) for searching YouTube videos.
- [MPV](https://mpv.io/) for playing videos in the framebuffer.
- Multimedia content with [ffmpeg](https://github.com/FFmpeg/FFmpeg)

  
### Image Viewer

- [FIM](https://www.nongnu.org/fbi-improved/) image viewer program for framebuffer.





