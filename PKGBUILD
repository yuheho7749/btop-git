# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.4.2
pkgrel=1
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/aristocratos/$pkgname"
license=(Apache-2.0)
depends=(gcc-libs
         glibc)
makedepends=(lowdown
             rocm-smi-lib)
optdepends=('rocm-smi-lib: AMD GPU support')
_archive="$pkgname-$pkgver"
source=("$url/archive/v$pkgver/$_archive.tar.gz")
sha256sums=('c7c0fb625af269d47eed926784900c8e154fdf71703f4325cffdf26357338c85')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

