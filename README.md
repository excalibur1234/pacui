# pacli
A simple and interactive Bash Frontend for Pacman/Yaourt

pacli is a CLI tool, which provides simple and advanced Pacman and Yaourt commands in an easy to use text interface. Additionally, it offers some Manjaro exclusive commands.

pacli is meant for experienced/intermediate/advanced users, who have basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices pacli provides.


## Screenshots

Home Screen of Pacli:
![Screenshot 01](http://i.imgur.com/eqXZWrC.png)

Downgrading the package "file-roller":
![Screenshot 02](http://i.imgur.com/kKzqbSl.png)


## Installation

### Installation from the AUR
Install [pacli from the AUR](https://aur.archlinux.org/packages/pacli/).

### Manual Installation
First, make sure all dependencies of pacli are installed on your system:
- pacman
- [yaourt](https://wiki.archlinux.org/index.php/Yaourt)
- [fzf](https://aur.archlinux.org/packages/fzf/)
- [downgrade](https://aur.archlinux.org/packages/downgrade/)
- bash
- sudo
- gzip
- git

Then, clone this Github repository to your system with the command:
```
git clone https://github.com/Manjaro-Pek/pacli
```
and execute pacli:
```
cd pacli && chmod +x pacli && ./pacli
```
