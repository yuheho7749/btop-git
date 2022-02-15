# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.2.2
pkgrel=1
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/aristocratos/$pkgname"
license=(Apache)
depends=(gcc-libs)
_archive="$pkgname-$pkgver"
source=("$url/archive/v$pkgver/$_archive.tar.gz")
sha256sums=('9e16b76ad74086948fa3dce4899a5532095a1656e6f1deec3e807f992d22f47c')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

