# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.1.0
pkgrel=1
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64 aarch64 i686)
url="https://github.com/aristocratos/$pkgname"
license=(Apache)
depends=(gcc-libs)
_archive="$pkgname-$pkgver"
source=("$_archive.tar.gz::$url/archive/v$pkgver.tar.gz")
sha256sums=('bcabd70cce6716386d3b4f798ba76f7a4a0a507fa11b8cf3e15c55ba139ebbd6')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

