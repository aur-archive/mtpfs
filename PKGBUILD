# Maintainer: yugrotavele <yugrotavele at archlinux dot us>
# Contributor: Anton Pirogov <anton.pirogov <AT> googlemail.com>

pkgname=mtpfs
pkgver=1.0
pkgrel=1
pkgdesc="A FUSE filesystem that supports reading and writing from any MTP device"
arch=('i686' 'x86_64')
url="http://www.adebenham.com/mtpfs/"
license=('GPL3')
depends=('libmtp>=0.3.0' 'glib2' 'libid3tag' 'fuse' 'libmad')
makedepends=('pkg-config')
source=(http://www.adebenham.com/debian/${pkgname}-${pkgver}.tar.gz)
md5sums=('7d62fdfdb59d87d115e2f804d0dc7f85')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}
