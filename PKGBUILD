# Maintainer: Static_Rocket

pkgname=lldb-debug-server
pkgver=0.0.3
pkgrel=1
pkgdesc="An LLDB debug server running as root to remotely debug (c,c++,rust) applications"
arch=('x86_64')
license=('GPL2')
depends=('lldb')
source=("lldb-debug-server.service")
b2sums=('a7aaa0e4a17477fb0e13b3dc66e8a62521a2aabfcbca85575032fe1d583e96658675b62798a72d36c8390d9ab4ab9f7afd7c549b0d0909da202ae882b8983701')

package() {
	mkdir -p "$pkgdir/usr/lib/systemd/system"
	mkdir -p "$pkgdir/var/lldb-debug-server"
	install -m 644 "$srcdir/lldb-debug-server.service" "$pkgdir/usr/lib/systemd/system"
}

