# PacUI

PacUI is a CLI tool, which provides useful and advanced Pacman and Yaourt/Pacaur commands in an easy to use text interface. If Pacaur is installed on your system, it will be used by default instead of Yaourt.

PacUI is meant for experienced/intermediate/advanced users, who have at least basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices PacUI offers.

This fork of an old version of [pacli](https://github.com/Manjaro-Pek/pacli/tree/f98e9226eb75ea00217481f436399328fe73d3ae) called PacUI follows the KISS principle: The whole program is contained within one file, which consists of easy to read bash code with many helpful comments. PacUI wants to provide the same or more functionality as pacli but without any available settings and/or translations. Additionally, PacUI does not require the use of the UI, but can also be used by terminal commands directly: This way of using PacUI is much faster!


## Screenshots

Home Screen of PacUI's UI:

![Screenshot 01](http://s28.postimg.org/vec8kajnx/screen_png.jpg)


Installing the package "cantata" from the Manjaro repositories:

![Screenshot 02](http://s32.postimg.org/50okof26t/pacli_simple2.gif)


New "conf" option, which lets you edit a lot of .conf files on your system:

![Screenshot 03](http://s27.postimg.org/mmb3ten1f/screen.png)


## Installation

Simply install the stable version of PacUI from the Manjaro repositories:
```
sudo pacman -S pacui
```

Alternatively, you can also install the latest version of PacUI:
```
yaourt -S pacui-git
```

This will install PacUI including the latest commits on Github. If you ever encounter any bugs, please reinstall (and thereby update) PacUI with the same command and check whether the bug is still there before reporting it.

It is highly recommended to use an utility, which notifies the user about available updates alongside of PacUI. Such a lightweight utility is for example [update-notifier](https://github.com/Chrysostomus/update-notifier).

### Execute without prior Installation
Alternatively, it is possible to download and start PacUI without prior installation using the following commands:
```
wget https://raw.githubusercontent.com/excalibur1234/pacui/master/pacui
```
```
bash pacui
```


## Use PacUI

### Start PacUI with UI
After successful installation, type the following command into your terminal in order to start PacUI with a nice UI:
```
pacui
```

### Start PacUI without UI: Using Options
For example, you want to display the **r**everse dependency **t**ree of a package. Please first note the marked letters "R" and "T" in PacUI's corresponding option when starting PacUI with UI.
PacUI does not care, whether you use upper or lower case letters as options or whether you use none, one or two dashes in front. Now, type one of the four equivalent choices into your terminal and press "ENTER": 
- `pacui RT`
- `pacui rt`
- `pacui -rt`
- `pacui --rt`

This principle can be used with all of PacUI's options. Here is another random example (of PacUI's "Pacman Log" option):
- `pacui LOG`
- `pacui -LOG`
- `pacui --LOG`
- `pacui log`
- `pacui -log`
- `pacui --log`

### Start PacUI without UI: Using Options and Package Names

You can also use package names in addition to options. For example, you want to install the package "cantata". Then, you can use a command like
```
pacui i cant
```
Instead of a list of all available packages, a much shorter already filtered list is displayed. Simply select the "cantata" package and press ENTER in order to install it.


Alternatively, you can use the command
```
pacui i cantat
```
Since there is only one package found in the Manjaro repositories when searching for "cantat", the list view is skipped and you are immediately prompted to install "cantata".

## Recommended Settings
Along with PacUI the following settings are recommended:

### Fancy List View
A fancy list view for all pacman updates can be enabled by uncommenting the following line in your /etc/pacman.conf file:
```
#VerbosePkgLists
```
A very easy way to edit this file by using PacUI is:
```
pacui conf pacman.conf
```

### Limit Mirrors Check to Countries Near You
Whenever pacman-mirrors is used by PacUI, e.g. in the "Clean System" option, your ping is checked to all Manjaro servers/mirrors. By limiting this check to mirrors near you, you can dramatically speed up this process.
You can achieve this by uncommenting and editing the line according to the tips above the following line in your /etc/pacman-mirrors.conf file:
```
#OnlyCountry =
```
A very easy way to edit this file by using PacUI is:
```
pacui --conf pacman-mirrors
```

### Alias
If you use PacUI without the UI it is recommended to use an alias for PacUI to reduce the amount of necessary typing. Do this by adding the following line to your ~.bashrc file (if you use bash):
```
alias p='pacui'
```
This will set "p" as an alias to "pacui" within your terminal (after a reboot of your system). This means that for updating your system, you can simply use
```
p u
```


## Help

### Short PacUI Help
For short help, e.g. when using PacUI without UI, use one of the following commands:
- `pacui h`
- `pacui -h`

### Detailed PacUI Help
Choose the "Help" option within PacUI's UI by entering "12" or "H" or "h" or "help" and pressing "ENTER".

This help page explains some general stuff such as how to navigate PacUI. It also explains every PacUI option in detail. If you want to look up which commands PacUI uses under the hood and understand them, this is the right place for you!

### Manjaro Forum Threads
 - [New Forum](https://forum.manjaro.org/t/pacui-a-simple-bash-frontend-for-pacman-and-yaourt-pacaur/677)
 - [Old Forum - Inactive Thread](https://classicforum.manjaro.org/index.php?topic=21399.0)
