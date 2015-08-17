# Maintainer: Antonio Rojas <nqn1976 @ gmail.com>

pkgname=ttf-oxygen
pkgver=0.3.96
_plasmaver=4.96.0
pkgrel=1
epoch=1
pkgdesc='A desktop/gui font family for integrated use with the KDE desktop.'
arch=('any')
install=$pkgname.install
source=(http://download.kde.org/unstable/plasma/$_plasmaver/src/oxygen-fonts-$pkgver.tar.xz)
license=('Open Font License 1.1')
url="https://projects.kde.org/projects/playground/artwork/oxygen-fonts"
makedepends=('extra-cmake-modules' 'qt5-base' 'fontforge')
depends=('fontconfig' 'xorg-fonts-encodings' 'xorg-font-utils')
provides=('ttf-font')
md5sums=('642f58a9d8dc99be50d421c468eeba6f')

build() {
  cd oxygen-fonts-$pkgver
  mkdir build
  cd build
  cmake .. -DCMAKE_INSTALL_PREFIX=/usr -DLIB_INSTALL_DIR=lib
  make
}


package() {
  cd oxygen-fonts-$pkgver/build
  make DESTDIR=${pkgdir} install  
}
