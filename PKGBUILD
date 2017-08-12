# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>
# Maintainer: excalibur1234 @forum.manjaro.org

pkgname=pacui
pkgver=1.6.1
pkgrel=1
pkgdesc="A simple and interative Bash Frontend for Pacman/Pacaur/Yaourt"
arch=(any)
url="https://github.com/excalibur1234/$pkgname"
license=('GPL3')
depends=('expac' 'wget' 'sudo' 'fzf')
conflicts=("$pkgname-git" 'pacli-simple')
replaces=('pacli-simple')
optdepends=('pacaur: Needed for AUR support. If installed, it gets used by default over Yaourt.'
        'yaourt: Needed for AUR support.'
        'pacman-mirrors: Needed for Manjaro mirror support'
        'reflector: Needed for Arch Linux mirror support'
        'downgrade: Needed for hidden "downgrade" option.')
source=("$url/archive/$pkgver.tar.gz")
md5sums=('1a36034db48ce0d93fa350e031534ee6')

# how to get md5sum:
#  1. do "updpkgsums" inside the folder of PKGBUILD
#  2. delete ...tar.gz file

package () {
	cd $srcdir
        install -Dm755 $srcdir/$pkgname-$pkgver/pacui $pkgdir/usr/bin/pacui
}
