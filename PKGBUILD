pkgname=st-metric-dt-git
_pkgname=st
pkgrel=3
pkgver=0.8.4c
pkgdesc='A simple virtual terminal emulator for X.'
arch=('any')
license=('MIT')
depends=(libxft)
url=https://github.com/MetriC-DT/st
source=('git://github.com/MetriC-DT/st')
_sourcedir=$pkgname-$pkgver
_makeopts="--directory=$_sourcedir"
sha1sums=('SKIP')

provides=("${_pkgname}")
conflicts=("${_pkgname}")

build() {
    cd "${_pkgname}"
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
    cd "${_pkgname}"
	make PREFIX=/usr DESTDIR="${pkgdir}" install
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
}
