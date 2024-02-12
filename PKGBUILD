# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.3.1
pkgrel=3
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/aristocratos/$pkgname"
license=(Apache)
depends=(gcc-libs
         glibc)
makedepends=(rocm-smi-lib)
optdepends=('rocm-smi-lib: AMD GPU support')
_archive="$pkgname-$pkgver"
source=("$url/archive/v$pkgver/$_archive.tar.gz"
	"$pkgname-cope-with-bogus-rocm-version.patch::$url/pull/761.patch")
sha256sums=('9e7faa30550137598a712fc28c1fb907e48a1fa1a5b2fa2f939195cf91e1816e'
            '0dd794f02f9098aa45ca44930bb3a553c392abc241fb2a1df38b694f82ba4c16')

prepare() {
	cd "$_archive"
	patch -p1 -i "../$pkgname-cope-with-bogus-rocm-version.patch"
}

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

