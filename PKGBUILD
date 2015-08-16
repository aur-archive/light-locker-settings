# Maintainer: Rob McCathie <korrode AT gmail>

pkgname=light-locker-settings
pkgver=1.5.0
pkgrel=1
pkgdesc="Just a simple settings dialog for light-locker"
arch=('any')
url="https://launchpad.net/${pkgname}"
license=('GPL3')
depends=('light-locker' 'python-gobject' 'python-psutil')
makedepends=('intltool')
source=("${url}/${pkgver%.*}/${pkgver}/+download/${pkgname}-${pkgver}.tar.bz2")
sha1sums=('87a1a0f34c5bd9f53b93d0a5f30153c1d5a34d69')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
