# Maintainer: 7Ji <pugokushin@gmail.com>

pkgname=git-mirrorer
pkgver=1.1.1
pkgrel=1
pkgdesc="To mirror git repos, and archive and checkout them with submodules included implicitly."
arch=('x86_64' 'aarch64')
url="https://github.com/7Ji/${pkgname}"
license=('AGPL3')
depends=('libgit2' 'libyaml' 'xxhash')
_srcname="${pkgname}-${pkgver}"
source=(
  "${_srcname}.tar.gz::${url}/archive/refs/tags/v${pkgver}.tar.gz"
)
sha256sums=(
  '4644d2c9bf1775648726d41af8a68aa633c3bfb3d1f0120487e44d2f0da56efc'
)

build() {
  cd "${_srcname}"
  make "VERSION=${pkgver}-ArchLinux-${pkgrel}"
}

package() {
  install -Dm755 "${srcdir}/${_srcname}/${pkgname}" -t "${pkgdir}/usr/bin/"
}