pkgname=st
pkgver=0.8.4b
pkgrel=2
pkgdesc='A simple virtual terminal emulator for X.'
arch=('any')
license=('MIT')
depends=(libxft)
url=https://github.com/MetriC-DT/st
source=('https://github.com/MetriC-DT/st/archive/refs/tags/v0.8.4c.tar.gz')
md5sums=(de6e016e2cd5c1847dce8d71730cca1e)
_sourcedir=$pkgname-$pkgver
_makeopts="--directory=$_sourcedir"

build() {
    make $_makeopts X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
    local installopts='--mode 0644 -D --target-directory'
    local shrdir="$pkgdir/usr/share"
    local licdir="$shrdir/licenses/$pkgname"
    local docdir="$shrdir/doc/$pkgname"
    make $_makeopts PREFIX=/usr DESTDIR="$pkgdir" install
    install $installopts "$licdir" "$_sourcedir/LICENSE"
    install $installopts "$docdir" "$_sourcedir/README.md"
    install $installopts "$shrdir/$pkgname" "$_sourcedir/st.info"
}
