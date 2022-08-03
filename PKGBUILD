# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

pkgname=glacier-contacts
pkgver=0.8.1
pkgrel=1
pkgdesc="QML based contacts application for nemomobile"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-contacts"
license=('BSD-3-Clause')
depends=('nemo-qml-plugin-thumbnailer'
	'nemo-qml-plugin-contacts'
	'nemo-qml-plugin-folderlistmodel'
	'glacier-gallery'
	'glacier-filemuncher'
	'contactsd'
	'nemo-qml-plugin-dbus'
	'qt5-glacier-app')
makedepends=( 'cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('54df07b97309a19d10ad1acd29b2191339d80d25720322ce80a277dbf44ccdd5')


build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make  all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
