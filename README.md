# pacli-simple
A simple and interactive Bash Frontend for Pacman and Yaourt.

pacli is a CLI tool, which provides useful and advanced Pacman and Yaourt commands in an easy to use text interface. Additionally, single options of pacli can be run directly in your terminal.

pacli is meant for experienced/intermediate/advanced users, who have at least basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices pacli provides.

This fork of pacli called pacli-simple follows the KISS principle: The whole program is contained within one file, which contains easy to read bash code. pacli-simple wants to provide the same functionality as pacli but without any available settings and/or translations.


It is highly recommended to use an utility, which notifies the user about available updates alongside of pacli. Such a lightweight utility is for example [update-notifier](https://github.com/Chrysostomus/update-notifier).


## Screenshots

Home Screen of pacli:

![Screenshot 01](http://imagizer.imageshack.com/img924/8197/bPKppR.png)


Installing the package "cantata" from the Manjaro repositories:

![Screenshot 02](http://s32.postimg.org/50okof26t/pacli_simple2.gif)


Downgrading the package "file-roller":

![Screenshot 03](http://i.imgur.com/kKzqbSl.png)


## Download / Git Clone

First, make sure all dependencies of pacli are installed on your system:
- pacman
- [yaourt](https://wiki.archlinux.org/index.php/Yaourt)
- [fzf](https://aur.archlinux.org/packages/fzf/) (fuzzy finder)
- [downgrade](https://aur.archlinux.org/packages/downgrade/)
- pacman-mirrorlist
- bash
- sudo
- gzip
- git
- wget
- [update-notifier](https://github.com/Chrysostomus/update-notifier) (optional dependency - will notify the user about available updates)

Then, clone this Github repository to your system with the command:
```
git clone https://github.com/excalibur1234/pacli-simple.git
```
and execute pacli:
```
cd pacli-simple && chmod +x pacli && ./pacli
```


## Use pacli

### Start pacli with an UI
In order to start pacli, you need to execute the "pacli" file inside your pacli-simple directory. When you followed the download instructions above, just execute:
```
~/pacli-simple/pacli
```

### Manual Installation
If you want to start pacli with a simple "pacli" command from anywhere in your terminal, you have to copy or move the "pacli" file into your /usr/bin/ directory. A command for doing this could be (when the above download instructions were followed):
```
sudo cp ~/pacli-simple/pacli /usr/bin/
```
Now, you type "pacli" into your terminal and pacli will start with an UI.

### Start pacli without an UI
After you manually installed pacli's bash file as described above, you can call pacli's options from your terminal without the need to start pacli's UI:

For example, you want to display the reverse dependency tree of a package, just type one of the three following choices into your terminal (note that the letters "R" and "T" are marked in pacli's corresponding option):
- `pacli rt`
- `pacli -rt`
- `pacli --rt`

This principle can be used with all options in pacli. Here are some random examples:
- `pacli --info`
- `pacli info`
- `pacli -i`
- `pacli l`
- `pacli log`
- `pacli --log`
- `pacli -log`
- `pacli -ua`

Only "pacli h" works differently when called from the command line instead of pacli's UI: "pacli h" will show a very short overview of all available commands.


## Help

### pacli Help
Choose the "Help" option within pacli's UI by entering "11" or "h" or "help" and pressing "ENTER". 

This help page explains a little bit about pacli. It also explains every pacli option in detail. If you want to look up which commands pacli uses and understand them, this is the right place for you!

### Manjaro Forum
There is a new and old thread in the Manjaro forums. Most of the discussion between the developers is going on there:
 - [New Forum](https://forum.manjaro.org/t/pacli-simple-a-simple-bash-frontend-for-pacman-and-yaourt/677)
 - [Old Forum - Inactive Thread](https://old.forum.manjaro.org/index.php?topic=21399.0)
