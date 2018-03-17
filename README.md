
# PacUI

PacUI provides useful and advanced Pacman and Trizen/Yay/Yaourt/Pikaur/Pacaur commands in a convenient and easy to use text interface.

PacUI is aimed at experienced/intermediate/advanced users of Arch Linux (and Arch-based distributions, including Manjaro), who have at least basic knowledge of their Linux system, Pacman and [Trizen](https://github.com/trizen/trizen)/[Yay](https://github.com/Jguer/yay)/[Yaourt](https://github.com/archlinuxfr/yaourt)/[Pikaur](https://github.com/actionless/pikaur)/[Pacaur](https://github.com/rmarquis/pacaur). Absolute beginners are probably overwhelmed by the amount of choices PacUI offers.

This fork of an [older version of pacli](https://github.com/Manjaro-Pek/pacli/tree/f98e9226eb75ea00217481f436399328fe73d3ae) called PacUI follows the KISS principle: The whole script is contained within one file, which consists of easy to read bash code with many helpful comments. PacUI offers many more features over pacli in order to enhance comfort and speed of CLI based package management.


Table of Contents
-----------------

   * [Screenshots](#screenshots)
   * [Installation](#installation)
      * [Execute without prior Installation](#execute-without-prior-installation)
   * [Usage](#usage)
      * [Start PacUI with UI](#start-pacui-with-ui)
      * [Start PacUI without UI: Using Options](#start-pacui-without-ui-using-options)
      * [Start PacUI without UI: Using Options and Package Names](#start-pacui-without-ui-using-options-and-package-names)
   * [Useful Tips and Recommended Settings](#useful-tips-and-recommended-settings)
      * [Fancy List View](#fancy-list-view)
      * [Alias](#alias)
      * [Search syntax](#search-syntax)
   * [Help](#help)
      * [Short PacUI Help](#short-pacui-help)
      * [Detailed PacUI Help](#detailed-pacui-help)
      * [Manjaro Forum Threads](#manjaro-forum-threads)


## Screenshots

UI of PacUI:

![Screenshot 01](https://s14.postimg.org/ekwbm4a0h/pacui.png)


Installing the package "cantata" from system repositories by entering its name:

![Screenshot 02](https://s14.postimg.org/sekob7cwh/cantata.gif)


## Installation

In Manjaro, you can simply install the stable version of PacUI:
```
sudo pacman -S pacui
```

Both the stable version and the latest git version of PacUI are available on the AUR:
```
yaourt -S pacui-git
```

This will install PacUI including the latest commits on Github. If you ever encounter any bugs, please reinstall (and thereby update) PacUI with the this command and check whether the bug is still there before reporting it.

Please note that PacUI optionally requires also [Trizen](https://github.com/trizen/trizen), [Yay](https://github.com/Jguer/yay), [Yaourt](https://github.com/archlinuxfr/yaourt), [Pikaur](https://github.com/actionless/pikaur), or [Pacaur](https://github.com/rmarquis/pacaur) to enable use of the AUR. If more than one AUR helper is installed, they are used in the same order as listed above.


### Execute without prior Installation
Because PacUI is contained within one file, it is easy to download and run without prior installation. For a minimal working version of PacUI, please install its dependencies [expac](https://github.com/falconindy/expac) and [fzf](https://github.com/junegunn/fzf). Marking the "pacui" file as executable is essential, too:
```
wget https://raw.githubusercontent.com/excalibur1234/pacui/master/pacui
```
```
chmod +x pacui
```
```
pacui
```
I find this feature of PacUI invaluable for fixing systems. Here are two examples:
- A large number of updates broke (parts of) the UI, e.g. xorg, window manager, or desktop environment. In this case, switching to a tty (with CTRL + ALT + F2), installing PacUI and using "Roll Back System" to roll back all the latest updates can fix the system (temporarily).
- A broken keyring makes it impossible to apply updates or install any packages. Executing PacUI without prior installation and using "Fix Pacman Errors" to fix the keyring and all related problems is the easiest and fastest solution I know of.


## Usage

### Start PacUI with UI
After successful installation, type the following command into your terminal in order to start PacUI with a simple UI:
```
pacui
```

### Start PacUI without UI: Using Options
Using PacUI without its UI requires less keystrokes and can therefore be much quicker. An overview of all PacUI options is displayed with `pacui h`.

For example, you want to display the **R**everse dependency **T**ree of a package. Please note the marked letters "R" and "T" in PacUI's corresponding UI option.
PacUI does not care, whether you use upper or lower case letters as options or whether you use no, one or two dashes in front. Therefore, the following four commands are equivalent:
- `pacui RT`
- `pacui rt`
- `pacui -rt`
- `pacui --rt`

This principle can be used with all of PacUI's options. Here is another random example (of PacUI's hidden "List Packages by Size" option):
- `pacui LS`
- `pacui -LS`
- `pacui --LS`
- `pacui ls`
- `pacui -ls`
- `pacui --ls`

### Start PacUI without UI: Using Options and Package Names

You can also use package names in addition to options. For example, you want to install the package "cantata". Then, you can use a command like
```
pacui i cantata
```
Instead of a list of all available packages, a much shorter already filtered list is displayed. Simply select the "cantata" package you want to install and press ENTER in order to install it.

If an argument contains special characters, it has to be quoted. For example when using regular expressions in order to search package file names starting with "zsh":
```
pacui s "^zsh"
```

## Useful Tips and Recommended Settings
It is highly recommended to use an utility, which notifies the user about available updates alongside of PacUI. Such a lightweight utility is for example [update-notifier](https://github.com/Chrysostomus/update-notifier).

Along with PacUI the following settings are recommended by the author:

### Fancy List View
A fancy list view for all pacman updates can be enabled by uncommenting the following line in your /etc/pacman.conf file:
```
#VerbosePkgLists
```
A very easy way to edit this file by using PacUI is:
```
pacui c pacman.conf
```


### Alias
If you use PacUI without the UI it is recommended to use an alias for PacUI to reduce the amount of necessary typing. Do this by adding the following line to your ~/.bashrc file (if you use bash):
```
alias p='pacui'
```
This will set "p" as an alias to "pacui" within your terminal (after a restart of your shell or computer). For example, you can now update your system using
```
p u
```

### Search syntax
PacUI uses [fuzzy finder (fzf)](https://github.com/junegunn/fzf) to display lists of items (such as packages, package groups, logs, patchs, etc.) and by starting to type, you can easily search/filter those lists. Regular expressions can be used to improve the search results, e.g.:

| Search Term | Description                       |
| ----------- | --------------------------------- |
|  `"sbtrkt"`   | Items that match `sbtrkt`         |
|  `"^music"`   | Items that start with `music`     |
|  `"git$"`     | Items that end with `git`         |
|  `"'wild"`    | Items that include `wild`         |
|  `"!fire"`    | Items that do not include `fire`  |
|  `"!-git$"`   | Items that do not end with `-git` |

A single bar character term acts as an OR operator. For example, the following query matches entries that start with `core` or end with `go`, `rb`, or `py`.
```
"^core|go$|rb$|py$"
```


## Help

### Short PacUI Help
For short help, e.g. when using PacUI without UI, use one of the following commands:
- `pacui h`
- `pacui -h`

### Detailed PacUI Help
Choose the "Help" option within PacUI's UI by entering "00" or "H" or "h" or "help" and pressing "ENTER".

This help page explains some general stuff such as how to navigate PacUI. It also explains every PacUI option in detail. If you want to look up which commands PacUI uses under the hood and understand them, this is the right place for you!

### Manjaro Forum Threads
 - [New Forum](https://forum.manjaro.org/t/pacui-a-simple-bash-frontend-for-pacman-and-yaourt-pacaur/677)
 - [Old Forum - Inactive Thread](https://classicforum.manjaro.org/index.php?topic=21399.0)
