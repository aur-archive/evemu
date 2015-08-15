# Maintainer: Nicolas Quiénot < niQo at aur >

pkgname=evemu
pkgver=1.0.10
pkgrel=4
pkgdesc="Tools and bindings for kernel input event device emulation and data capture and replay."
arch=(i686 x86_64)
url="https://launchpad.net/evemu"
license=(GPL)
depends=('glibc' 'python2')
provides=('utouch-evemu')
conflicts=('utouch-evemu')
replaces=('utouch-evemu')
options=('!libtool')
source=(http://launchpad.net/$pkgname/trunk/$pkgname-$pkgver/+download/$pkgname-$pkgver.tar.gz)

build() {
  cd "$srcdir/$pkgname-$pkgver"

  PYTHON=/usr/bin/python2 ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}

md5sums=('2291627ed85aaad375b7f3ef531ce57b')
