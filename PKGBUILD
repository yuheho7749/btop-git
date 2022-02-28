# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.2.4
pkgrel=1
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/aristocratos/$pkgname"
license=(Apache)
depends=(gcc-libs)
_archive="$pkgname-$pkgver"
source=("$url/archive/v$pkgver/$_archive.tar.gz")
sha256sums=('33bd5ff614926aab3a08803f507e7bf19983fd263b3f216c2884cd51cfc3d283')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

