# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.2.3
pkgrel=1
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/aristocratos/$pkgname"
license=(Apache)
depends=(gcc-libs)
_archive="$pkgname-$pkgver"
source=("$url/archive/v$pkgver/$_archive.tar.gz")
sha256sums=('8348bb37b642bf899b5ce0850d64e12cf9671c8c9624f3d21b58a015cd502107')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

