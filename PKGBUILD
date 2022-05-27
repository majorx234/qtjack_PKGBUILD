pkgname=qtjack
pkgdesc="qt jack library to use jack realtime audio processing in QT projects"
pkgver=1.0.4
pkgrel=1
arch=("x86_64" "arm7h")
url="https://github.com/majorx234/qtjack"
license=("GPLv3")
depends=("qt5-base" "jack")
makedepends=("qt5-base")
source=("git+https://github.com/majorx234/qtjack.git#tag=$pkgver")
sha256sums=('SKIP')

build() {
[ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        ${srcdir}/${pkgname}
  make      
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}
