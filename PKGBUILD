pkgname=st
pkgver=0.8.4a
pkgrel=1
pkgdesc="Custom patch fork of st terminal"
arch=('any')
url=https://github.com/MetriC-DT/st
license=('MIT')
depends=('libxft')
source=('https://github.com/MetriC-DT/st/archive/refs/tags/v0.8.4a.tar.gz')
md5sums=('a0f510c26331210b11aa69c5d8d2c837')
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
