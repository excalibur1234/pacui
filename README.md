# pacli-simple
A simple and interactive Bash Frontend for Pacman/Yaourt

pacli is a CLI tool, which provides simple and advanced Pacman and Yaourt commands in an easy to use text interface. Additionally, it offers some Manjaro exclusive commands.

pacli is meant for experienced/intermediate/advanced users, who have basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices pacli provides.

This fork of pacli called pacli-simple follows the KISS principle: The whole program is contained within one file, which contains easy to read bash code. pacli-simple wants to provide the same functionality as pacli but without any available settings and/or translations.


It is highly recommended to use an utility, which notifies the user about available updates alongside of pacli. Such a lightweight utility is for example [update-notifier](https://github.com/Chrysostomus/update-notifier).


## Screenshots

Home Screen of pacli:
![Screenshot 01](http://imagizer.imageshack.com/img924/7457/zoU5u2.png)

Installing the package "cantata" from the Manjaro repositories:
![Screenshot 02](http://imagizer.imageshack.com/img923/4341/rlbOYN.png)

Removing "qt4" and another package from my system:
![Screenshot 03](http://i.imgur.com/jJKrdp5.png)

Downgrading the package "file-roller":
![Screenshot 04](http://i.imgur.com/kKzqbSl.png)

Looking up what packages on my system depend on "gtk2":
![Screenshot 05](http://i.imgur.com/dVfXdLj.png)


## Installation / Git Clone

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
In order to start pacli, you need to execute the "pacli" file in your pacli directory. When you followed the installation instructions above, just go to your home directory and execute:
```
./pacli-simple/pacli
```

If you want to start pacli with a simple "pacli" command from anywhere in your terminal, you have to copy or move the "pacli" file into your /usr/bin/ directory. A command for doing this could be (when the above installation was followed):
```
sudo cp ~/pacli-simple/pacli /usr/bin/
```
Now, you type "pacli" into your terminal and pacli will start.

You can also type "pacli i" (note that "i" is marked in pacli's option no. 3) into your terminal and pacli's option 3 will execute without pacli being started. This command can be used with all marked options in pacli, for example: "pacli fua", "pacli l", "pacli log", etc.


## Help

### pacli Help
Choose the "Help" option within pacli by entering "11" or "h" or "help" and pressing "ENTER". 

This help page explains a little bit about pacli. It also explains every pacli option in detail. If you want to look up which commands pacli uses and understand them, this is the right place for you!

### Manjaro Forum
There are 2 threads in the Manjaro forum. Most of the discussion between the developers is going on there:
 - [Main Thread](https://forum.manjaro.org/index.php?topic=21399.0)
 - [Additional Thread](https://forum.manjaro.org/index.php?topic=28563.0)
