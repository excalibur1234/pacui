# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>
# Maintainer: excalibur1234 @forum.manjaro.org

pkgname=pacui
pkgver=1.5
pkgrel=1
pkgdesc="A simple and interative Bash Frontend for Pacman/Pacaur/Yaourt"
arch=(any)
url="https://github.com/excalibur1234/$pkgname"
license=('GPL3')
depends=('package-query' 'wget' 'gawk' 'sudo' 'fzf')
conflicts=("$pkgname-git" 'pacli-simple')
replaces=('pacli-simple')
optdepends=('pacaur: Needed for AUR support. If installed, it gets used by default over Yaourt.'
        'yaourt: Needed for AUR support.'        
        'downgrade: Needed for hidded "downgrade" option.')
source=("$url/archive/$pkgver.tar.gz")
md5sums=('6298f8f3a33b4e338b11607b89532291')

# how to get md5sum:
#  do "updpkgsums" inside the folder of PKGBUILD

package () {
	cd $srcdir
        install -Dm755 $srcdir/$pkgname-$pkgver/pacui $pkgdir/usr/bin/pacui
}
