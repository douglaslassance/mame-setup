# MAME

### Enquire

[MAME](http://www.mamedev.org) is an amazing program that emulate pretty much every arcade system that ever existed. The only issue is that it can be a bit complicated to setup and a lot of the helpers softwares gravitating around it are imperfect or incomplete. Many friends always ask me to set it up for them and I got tired to maintain these installations. Git version control seemed to be a good way for me to distribute the setup and have my friend update it easily.

### Install

This folder is meant to be merged on top of an official download of the MAME 0.229 emulator. On **Windows** you'll simply have to [download](https://github.com/mamedev/mame/releases/download/mame0229/mame0229b_64bit.exe) and unzip the program. On **MacOS** we rely on SLDMAME that you can be downloaded [here](https://sdlmame.lngn.net/mame0229-64bit.zip). As the name indicates, this flavor of MAME relies on the [SDL framework](https://www.libsdl.org/download-2.0.php) which will also have to be installed before you can run the emulator. Installation is pretty straight forward but this [video tutorial](http://youtu.be/K6xyO-poAZU?t=30s) may help.

### Launch

If you want to use the GUI simply double-click the executable. Press <kbd>Alt</kbd> + <kbd>Enter</kbd> to go fullscreen. If you want to use the commands, keep reading. Using a terminal, `cd` to the `mame` folder and run `./mame [rom_name]` for example `./mame sfa3`. Since version 0.226, MAME emulates consoles, therefore you can also run `./mame [machine_bios] [rom_name]` for example `./mame megadriv sor2`. You will notice that MAME will conveniently propose rom name corrections if you type something slightly wrong. I use that all the time. There is a lot of other possibilities when running the emulator through command line and you can have a better idea of what is available by running `mame -h`.

### Play

You can play with the keyboard but the emulator is also already configured to work with four [8BitDo Arcade Sticks](https://www.8bitdo.com/arcade-stick/). Main keyboard keys for the first player are <kbd>1</kbd> for start, <kbd>5</kbd> to insert coin, <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> for movement and <kbd>G</kbd> <kbd>H</kbd> <kbd>J</kbd> <kbd>B</kbd> <kbd>N</kbd> <kbd>M</kbd> for buttons. The other players are only mapped to joysticks.

### Extend

An emulator is not worth much without it's roms, unfortunately I cannot provide them as part of that setup for obvious reasons. Therefore you will have to use you imagination to get a hold on these little gems. Once you do, create a `roms` folder at the root of the `mame` folder and stick all the `.zip` files in there. Console BIOS roms should also go in the `roms` folder, on the other hand, console game roms should go in a separate folder called `soft` and should be grouped by systems such as `megadriv`.

A few game developer have been kind enough to declare there game non-commercial and therefore these [roms](http://www.mamedev.org/roms/) can be downloaded in a totally official manner.
