# pacli-simple

pacli is a CLI tool, which provides useful and advanced Pacman and Yaourt commands in an easy to use text interface. 

pacli is meant for experienced/intermediate/advanced users, who have at least basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices pacli offers.

This fork of an old version of [pacli](https://github.com/Manjaro-Pek/pacli) called pacli-simple follows the KISS principle: The whole program is contained within one file, which contains easy to read bash code. pacli-simple wants to provide the same functionality as pacli but without any available settings and/or translations. Additionally, pacli-simple does not require the use of the UI, but can also be used by terminal commands directly: This way of using pacli is much faster!


## Screenshots

Home Screen of pacli:

![Screenshot 01](http://s18.postimg.org/8dz7xjlzt/screen.png)


Installing the package "cantata" from the Manjaro repositories:

![Screenshot 02](http://s32.postimg.org/50okof26t/pacli_simple2.gif)


Downgrading the package "file-roller":

![Screenshot 03](http://i.imgur.com/kKzqbSl.png)


New "conf" option, which lets you edit a lot of .conf files on your system:

![Screenshot 04](https://s18.postimg.org/5jgervr7t/conf.png)


## Installation

Simply install pacli-simple from the AUR:
```
yaourt -S pacli-simple
```

It is highly recommended to use an utility, which notifies the user about available updates alongside of pacli. Such a lightweight utility is for example [update-notifier](https://github.com/Chrysostomus/update-notifier).


## Use pacli

### Start pacli with UI
Type the following command into your terminal in order to start pacli with a nice UI:
```
pacli
```

### Start pacli without UI: Using Options
For example, you want to display the **r**everse dependency **t**ree of a package. Please first note the marked letters "R" and "T" in pacli's corresponding option when starting pacli with UI.
Now, type one of the three following choices into your terminal and press "ENTER". pacli does not care, whether you use upper or lower case letters as options or whether you use nonw, one or two dashes in front:
- `pacli rt`
- `pacli -rt`
- `pacli --rt`

This principle can be used with all of pacli's options. Here are some random examples:
- `pacli l`
- `pacli -l`
- `pacli log`
- `pacli -log`
- `pacli --log`

### Start pacli without UI: Using Options and Package Names

You can also use package names in addition to options. For example, you want to install the package "cantata". Then, you can use a command like
```
pacli i cant
```
Instead of a list of all available packages, a much shorter already filtered list is displayed. Simply select the "cantata" package and press ENTER in order to install it.


Alternatively, you can use the command
```
pacli i cantata
```
Since there is only one package called "cantata" in the Manjaro repositories available, fuzzy finder is skipped and you are immediately prompted to install "cantata".


## Help

### Short pacli Help
For quick and very short help, e.g. when using pacli without UI, use one of the following commands:
- `pacli h`
- `pacli -h`

### Detailed pacli Help
Choose the "Help" option within pacli's UI by entering "11" or "h" or "help" and pressing "ENTER".

This help page explains some general stuff such as how to navigate in pacli. It also explains every pacli option in detail. If you want to look up which commands pacli uses under the hood and understand them, this is the right place for you!

### Manjaro Forum
There are new and old topics in the Manjaro forum. Most of the discussion between the developers is going on there:
 - [New Forum](https://forum.manjaro.org/t/pacli-simple-a-simple-bash-frontend-for-pacman-and-yaourt/677)
 - [Old Forum - Inactive Thread](https://classicforum.manjaro.org/index.php?topic=21399.0)
