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
- Personal page: https://github.com/kyberszittya/personal-page, commit: https://github.com/kyberszittya/personal-page/commit/a00a7acdab959aeb27d18e38ff8ae867e9762117


### Day 1: September 25, 2024

**Today's Progress**: This day was a little tiring. Nevertheless: made some progress with creating a Spring Boot backend (with dummy security). Also started Projects page on Personal Page.

**Thoughts:** : nothing extraordinary. Previously I had exposure to Spring Boot. The only problem it caused, to install Java 23 and IntelliJ for proper work.


**Link to work:**
- Personal page: https://github.com/kyberszittya/personal-page, commit: https://github.com/kyberszittya/personal-page/commit/10630dfcd50b057d115e69dec9177616eee011dc


### Day missed: September 26, 2024

**Today's Progress**: I was back in work and I had tremendous work, finished in the night. Today was unfortunately missed.

### Day missed: September 27, 2024

**Today's Progress**: I was back in work at my second workplace (had a one day event till late night), so I missed this as I arived around midnight at home. Better do work with fresh mind.

### Day 2: September 28, 2024

**Today's Progress**: Finished the calendar component on the Personal page, serving blog entries by Spring (in Hibernate for now).

**Thoughts:** : the calendar component had its strange behavior, especially when Spring was used to store the blog entries. 

**Link to work:**
- Personal page: https://github.com/kyberszittya/personal-page, commit: https://github.com/kyberszittya/personal-page/commit/79c52af3e6f1da52d0dae78c92ca814083972772

### Day 3: September 29, 2024

**Today's progress**: Using PostgreSQL instead of H2.

**Thoughts**: granting access for read only user is a good thing.

**Link to work:**
- Personal page: https://github.com/kyberszittya/personal-page, commit: https://github.com/kyberszittya/personal-page/commit/3e7114e9c5d19e0f79b36180a1d02b9af89c5a56

### Day 4: September 30, 2024

**Today's progress**: Just a simple refresher in OpenCV and PyQT.

**Thoughts**: PyQT and ChatGPT suits well together.

**Link to work:**
- 100 days of AI: https://github.com/kyberszittya/100days-ai, commit: https://github.com/kyberszittya/100days-ai/commit/6fdaa6fc54f7e73799c65e0f9e9d3ebf76fba561

### Day 5: October 1, 2024

**Today's progress**: Login page on personal page. Also started to add a new post creation on the blog.

**Thoughts**: Routers. Routers everywhere.

**Link to work:**
- Personal page: https://github.com/kyberszittya/personal-page, commit: https://github.com/kyberszittya/personal-page/commit/b60ef8dc448cf24d8a158df66fd686a58389f61d, commit: https://github.com/kyberszittya/personal-page/commit/6bfd3acc48e0558344de1f0092b2ed0c10f38198

