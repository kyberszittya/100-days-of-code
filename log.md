# 100 Days Of Code - Log

## Week 1

First of all, I have a great aid: my own personal data analyzer ChatGPT persona, called Tiwaz-A0. 

Check it out here: https://chatgpt.com/g/g-hxly0oNgz-tiwaz-a0

__Current location__: Hungary, GMT+02

### Planned outline of Week 1

_Main task:_ STM32 Development Environment Setup & Frontend Framework Setup

### Day 0: September 24, 2024

**Today's Progress**: CubeMX and STMCubeIDE installed, uploaded blinking LED project to the board. Configured 108 MHz system clock. PB0 (GPIO) & PA0 (PWM output) used as configured pins. More information in the utility notebooks. Also get some fancy starting website with next.js (loving that framework).

**Thoughts:** : of course, nothing is so easy, as it seems originally. On Ubuntu 24.04, ncurses 5 is not available, the following workaround works (source: https://community.st.com/t5/stm32cubeide-mcus/stm32cubeide-requires-libncurses-so-5-which-is-not-provided-on/m-p/91286/highlight/true#M2319), by downloading and building the ncurses5 from source:
```bash
#!/bin/bash
 
wget "https://ftp.gnu.org/pub/gnu/ncurses/ncurses-6.3.tar.gz"
tar -xvf ncurses-6.3.tar.gz
cd ncurses-6.3
 
# args taken from `https://src.fedoraproject.org/rpms/ncurses/blob/f36/f/STAGE2-ncurses`
./configure --prefix=/usr/local \
    --with-shared --without-ada --with-ospeed=unsigned \
    --with-terminfo-dirs=/etc/terminfo:/usr/share/terminfo \
    --enable-hard-tabs --enable-xmc-glitch --enable-colorfgbg \
    --enable-overwrite \
    --enable-pc-files \
    --disable-wattr-macros \
    --with-termlib=tinfo \
    --with-chtype=long \
    --with-ticlib \
    --with-abi-version=5 # ABI version 5 produces `libncurses.so.5`
 
make
sudo make install
```
After local installation, debugging and uploading is all OK.

**Link to work:**
- Embedded: https://github.com/kyberszittya/100days-embedded
- Personal page: https://github.com/kyberszittya/personal-page


### Day 1: September 25, 2024

**Today's Progress**: 
