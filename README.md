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

Looking up what packages on my system depend on "gtk2":
![Screenshot 04](http://i.imgur.com/dVfXdLj.png)


## Download / Git Clone

First, make sure all dependencies of pacli are installed on your system:
- pacman
- [yaourt](https://wiki.archlinux.org/index.php/Yaourt)
- [fzf](https://aur.archlinux.org/packages/fzf/)
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

### Start pacli with a GUI
In order to start pacli, you need to execute the "pacli" file inside your pacli-simple directory. When you followed the download instructions above, just go to your home directory and execute:
```
./pacli-simple/pacli
```

### Manual Installation
If you want to start pacli with a simple "pacli" command from anywhere in your terminal, you have to copy or move the "pacli" file into your /usr/bin/ directory. A command for doing this could be (when the above download instructions were followed):
```
sudo cp ~/pacli-simple/pacli /usr/bin/
```
Now, you type "pacli" into your terminal and pacli will start with a GUI.

### Start pacli without a GUI
After you manually installed pacli's bash file as described above, you can also type "pacli i" (note that "i" is marked in pacli's install option) into your terminal and pacli's install option will execute without pacli being started. This sort of command can be used with all options in pacli, for example: "pacli info", "pacli l", "pacli log", etc.
Only "pacli h" works differently when called from the command line instead of pacli's GUI: "pacli h" will show an overview of all available commands.


## Help

### pacli Help
Choose the "Help" option within pacli by entering "11" or "h" or "help" inside pacli's GUI and pressing "ENTER". 

This help page explains a little bit about pacli. It also explains every pacli option in detail. If you want to look up which commands pacli uses and understand them, this is the right place for you!

### Manjaro Forum
There are 2 threads in the Manjaro forum. Most of the discussion between the developers is going on there:
 - [Main Thread](https://forum.manjaro.org/index.php?topic=21399.0)
 - [Additional Thread](https://forum.manjaro.org/index.php?topic=28563.0)
