# Maintainer: Static_Rocket

pkgname=lldb-debug-server
pkgver=0.0.2
pkgrel=1
pkgdesc="An LLDB debug server running as root to remotely debug (c,c++,rust) applications"
arch=('x86_64')
license=('GPL2')
depends=('lldb')
source=("lldb-debug-server.service")
md5sums=('SKIP')

package() {
	mkdir -p "$pkgdir/usr/lib/systemd/system"
	mkdir -p "$pkgdir/var/lldb-debug-server"
	install -m 644 "$srcdir/lldb-debug-server.service" "$pkgdir/usr/lib/systemd/system"
}

