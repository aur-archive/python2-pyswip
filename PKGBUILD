# Maintainer: Alexander Rødseth <rodseth@gmail.com>
# Contributor: p2k <patrick.schneider@uni-ulm.de>

pkgname=python2-pyswip
pkgver=0.2.3
pkgrel=1
pkgdesc='Python wrapper for SWI-Prolog'
arch=('x86_64' 'i686')
url='http://code.google.com/p/pyswip/'
license=('MIT')
provides=('pyswip')
replaces=('pyswip')
source=("http://pyswip.googlecode.com/files/pyswip-$pkgver.tar.gz")
depends=('python2' 'swi-prolog')
makedepends=('setuptools')
sha256sums=('dfaf68aeb04c9388d5f11311cacaab95f9a72a73f7a0595ac477e17545353b9d')

build() {
  cd "pyswip-$pkgver"
  python2 setup.py build
}

package() {
  cd "pyswip-$pkgver"
  python2 setup.py install --prefix=/usr --root="$pkgdir"
  mkdir -p "$pkgdir/usr/share/$pkgname"
  cp -R README examples "$pkgdir/usr/share/$pkgname"
}

# vim:set ts=2 sw=2 et:
