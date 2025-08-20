# Maintainer: yuheho7749 <yuheho7749 at gmail dot com>

_pkgname=btop
pkgname=$_pkgname-git
pkgver=1.4.4
pkgrel=4
pkgdesc='A monitor of system resources, bpytop ported to C++'
arch=(x86_64)
url="https://github.com/yuheho7749/$_pkgname"
license=(Apache-2.0)
depends=(gcc-libs
         glibc)
makedepends=(lowdown
             rocm-smi-lib)
optdepends=('rocm-smi-lib: AMD GPU support')
conflicts=('btop')

source=("$_pkgname::git+$url.git")
sha256sums=("SKIP")

build() {
	cd "$_pkgname"
	make all
}

package() {
	cd "$_pkgname"
	make DESTDIR="$pkgdir" PREFIX=/usr install
	make DESTDIR="$pkgdir" PREFIX=/usr setcap
}

