# MAME

[MAME](http://www.mamedev.org) is an amazing program that emulates pretty much every arcade system that existed. The only issue is that it can be a bit complicated to setup and a lot of the helpers softwares gravitating around it are imperfect or incomplete. Friends always ask me to set it up for them and I got tired to maintain these installations. Git seemed a good way for me to distribute the setup and them update easily.

### Installation

#### Windows

After installing [Scoop](https://scoop.sh), run the following commands in the [terminal](https://apps.microsoft.com/detail/9n0dx20hk701?hl=en-US&gl=US).

```bash
scoop bucket add emulators https://github.com/borger/scoop-emulators.git
scoop install git mame
git clone https://github.com/douglaslassance/mame-setup.git %%USERPROFILE\.mame
```

#### macOS

After installing [Homebrew](https://brew.sh/), run the following commands in the terminal.

```sh
brew install mame
git clone https://github.com/douglaslassance/mame-setup.git ~/.mame
```

### Launching

#### Windows

```
cd %USERPROFILE%\.mame && mame --rompath <path_to_roms> <rom_name>
```

#### macOS

```shell
cd ~/.mame && mame --rompath <path_to_roms> <rom_name>
```

> [!Note]
> It's recommanded to turn these commands into a terminal alias on macOS and PATH accessible batch file on Windows. That way you'll be able to simply type `mame <rom_name>` to start playing.

You're expected to pass a location for the roms since for copyright reason I cannot provide them as part of this setup. You'll have to collect these gems yourself.

A few game developers have been kind enough to declare there game non-commercial and therefore these [roms](http://www.mamedev.org/roms/) can be downloaded in a totally official manner.

Zipped arcade roms should live at the root of your roms folder, while console ones should live in a system sub-folder (ie. `nes`, `megadriv`, `snes`, etc.).

> [!Note]
> MAME will conveniently propose rom name corrections if you type something slightly wrong. It's a actually a convenient a way to find the actual rom name.

### Playing

You can play with the keyboard. Keys for the first player are <kbd>1</kbd> for start, <kbd>5</kbd> to insert coin, <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> for movement and <kbd>G</kbd> <kbd>H</kbd> <kbd>J</kbd> <kbd>B</kbd> <kbd>N</kbd> <kbd>M</kbd> for buttons. The other players are only mapped to joysticks.

The emulator is also already configured to work with four [8BitDo Arcade Sticks](https://www.8bitdo.com/arcade-stick/) in `X` mode for arcade games and with four [8BitDo Pro 2](https://www.8bitdo.com/pro2/) in `X` mode for consoles.

> [!Note]
> Other controller profiles like [RetroPort](https://www.retrousb.com/) ones are provided and can be found in the `ctrl` folder. You can override which profile is used by adding `--ctrlr <profile_name>` at the end of your `mame` command.

### Graphics

A pretty solid CRT filter is provided but de-activated by default. You can activate it by uncommenting the `glsl_shader_mame1` line in `mame.ini`.
