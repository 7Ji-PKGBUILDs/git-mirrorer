# Maintainer: 7Ji <pugokushin@gmail.com>

pkgname=git-mirrorer
pkgver=1.1.0
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
  '82a62e03bbf8b12e82f8bd1017c5acfed7f28208cab0a72c80e2d2816385f26d'
)

build() {
  cd "${_srcname}"
  make "VERSION=${pkgver}-ArchLinux-${pkgrel}"
}

package() {
  install -Dm755 "${srcdir}/${_srcname}/${pkgname}" -t "${pkgdir}/usr/bin/"
}