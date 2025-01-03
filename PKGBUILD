# Maintainer: Laura Demkowicz-Duffy <dev[at]demkowiczduffy.co.uk>
pkgname=zigup-bin
_pkgname=zigup
pkgver=v2025_01_02
pkgrel=3
pkgdesc="Download and manage zig compilers"
arch=('x86_64' 'aarch64' 'armv7h' 'riscv64')
url="https://github.com/marler8997/zigup"
license=('MIT-0')
provides=('zigup' 'zig')
conflicts=('zigup' 'zig')
install="$_pkgname.install"
source=("$url/archive/refs/tags/$pkgver.tar.gz")
source_x86_64=("$url/releases/download/$pkgver/zigup-x86_64-linux.tar.gz")
source_aarch64=("$url/releases/download/$pkgver/zigup-aarch64-linux.tar.gz")
source_armv7h=("$url/releases/download/$pkgver/zigup-arm-linux.tar.gz")
source_riscv64=("$url/releases/download/$pkgver/zigup-riscv64-linux.tar.gz")
sha256sums=('0b92de2a3afcecbf086102733215640189d744c4a17064b7492059ac198dd7f6')
sha256sums_x86_64=('1413d8369a34284bae39d17c9488634c89122181d831006bc1ea22f68e505522')
sha256sums_aarch64=('22f87b8c700bbe98795b2f55b0517e72d768166246995193c572854a9f5b2cec')
sha256sums_armv7h=('fc65fdeac8d5a2d39fa44cbecccd7af428e27072be78fe2650e5639e3708cc09')
sha256sums_riscv64=('99e167e30b9f2b0a1e6940a4fab3638a8949ded9c7cedec03062b25ea2b2e1a6')

package() {
    install -Dm 0755 $_pkgname $pkgdir/usr/bin/$_pkgname

    cd "$_pkgname-$(echo $pkgver | sed 's/^v//')"
    install -Dm 0644 README.md $pkgdir/usr/share/doc/$pkgname/README.md
    install -Dm 0644 LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
