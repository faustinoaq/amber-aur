# Maintainer: Faustino Aguilar <faustinoaq.github.io>
pkgname=amber
pkgver=0.2.5
pkgrel=1
pkgdesc="An open source efficient, cohesive and fun web framework for the Crystal language "
arch=(i686 x86_64)
url='https://github.com/amberframework/amber'
license=(MIT)
depends=('crystal' 'shards' 'sqlite')
source=("https://github.com/amberframework/amber/archive/v$pkgver.tar.gz")
sha256sums=('1743bc45afa170763102879e459d79b565bdabf189faca2559955385bb8d0c30')

build() {
  cd "amber-$pkgver"
  shards
  make build
}

package() {
  cd "amber-$pkgver"
  install -Dm755 bin/amber "$pkgdir/usr/bin/amber"
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/amber/LICENSE
}
