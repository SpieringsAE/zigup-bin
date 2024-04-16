# Maintainer: Laura Demkowicz-Duffy <dev[at]demkowiczduffy.co.uk>
pkgname=zigup-bin
_pkgname=zigup
pkgver=v2024_03_13
pkgrel=1
pkgdesc="Download and manage zig compilers"
arch=('x86_64')
url="https://github.com/marler8997/zigup"
license=('MIT-0')
provides=('zigup' 'zig')
conflicts=('zigup' 'zig')
source=(
    "$url/releases/download/$pkgver/zigup.ubuntu-latest-x86_64.zip"
    "$url/archive/refs/tags/$pkgver.tar.gz"
)
sha256sums=('8b05403e5b58ecd6a221251a884513e3f035d67e122bf11594633da6579a7133'
            '219a3e0fb391e85578033445e6dd57699b71da97cea56a4db1995017324113a3')

package() {
    install -Dm 0755 $_pkgname $pkgdir/usr/bin/$_pkgname
    install -Dm 0644 $_pkgname-$(echo $pkgver | sed 's/^v//')/README.md $pkgdir/usr/share/doc/$pkgname/README.md
}
