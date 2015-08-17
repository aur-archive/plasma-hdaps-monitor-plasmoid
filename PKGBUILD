# Maintainer: Michael Duell <mail@akurei.me> PGP-Key: 6EE23EBE
# Contributor: vogo

pkgname=plasma-hdaps-monitor-plasmoid
pkgver=0.3
pkgrel=3
pkgdesc="A small plasmoid to display the state of your harddisk protected with the hdapsd"
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/HDAPS+monitor?content=103481"
license=('GPL')
depends=('kdebase-workspace>=4.2.0' 'hdapsd')
makedepends=('gcc' 'cmake' 'automoc4')
source=("http://kde-look.org/CONTENT/content-files/103481-hdaps_monitor-$pkgver.tar.gz")

build() {
  cd "$srcdir/hdaps_monitor-$pkgver"
  mkdir build
  cd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr .. || return 1
  make || return 1
  make DESTDIR="$pkgdir/" install || return 1
}

sha512sums=('2fe1b57c751c68396d6a5d893e4746268cb3919a5a816ba0c38154164d12c282f5e2b043e5df1faaad5850a8fdf12a53e4eb07045dae0142c53d56ce99549ee4')
