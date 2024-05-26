# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

pkgname=glacier-contacts
pkgver=0.9
pkgrel=1
pkgdesc="QML based contacts application for nemomobile"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-contacts"
license=('BSD-3-Clause')
depends=('nemo-qml-plugin-thumbnailer'
	'nemo-qml-plugin-contacts'
	'nemo-qml-plugin-folderlistmodel'
	'glacier-gallery>=0.4'
	'glacier-filemuncher>=0.4'
	'nemo-qml-plugin-dbus'
	'qt6-glacier-app')
makedepends=( 'cmake' 'qt6-tools' 'clang')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('e8383089b3ee8339c5ec72df62baf662230461d31bbda8ce77e6d0973cd713ba')

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
