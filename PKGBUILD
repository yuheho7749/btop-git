# Maintainer: Caleb Maclennan <caleb@alerque.com>

pkgname=btop
pkgver=1.4.1
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
sha256sums=('40f6c54d1bc952c674b677d81dd25f55b61e9c004883c27950dc30780c86f381')

build() {
	cd "$_archive"
	make all
}

package() {
	cd "$_archive"
	make DESTDIR="$pkgdir" PREFIX=/usr install
}

