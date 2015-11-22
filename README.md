# pacli
A simple and interative Bash Frontend for Pacman/Yaourt

pacli is a CLI tool, which provides simple and advanced Pacman and Yaourt commands in an easy to use text interface. Additionally, it offers some Manjaro exclusive commands.

pacli is meant for experienced/intermediate/advanced users, who have basic knowledge of the structure of their Linux system and how Pacman and Yaourt work. Absolute beginners are probably overwhelmed by the amount of choices pacli provides.


## Screenshot
![Screenshot 01](https://i.imgur.com/hwGmDeKiO.png)
[Imgur](http://i.imgur.com/eqXZWrC.png)
[Imgur](http://i.imgur.com/Q2um0ac.png)
[Imgur](http://i.imgur.com/wbO9LmB.png)
[Imgur](http://i.imgur.com/kKzqbSl.png)
<blockquote class="imgur-embed-pub" lang="en" data-id="kKzqbSl"><a href="//imgur.com/kKzqbSl">View post on imgur.com</a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>

## Installation

### Installation from the AUR
Install [pacli from the AUR](https://aur.archlinux.org/packages/pacli/).

### Installation by hand
First, make sure all dependencies of pacli are installed on your system:
- pacman
- [yaourt](https://wiki.archlinux.org/index.php/Yaourt)
- [pmenu](https://aur.archlinux.org/packages/pmenu/)
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
