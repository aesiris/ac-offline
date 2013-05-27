# Maintainer: aesiris

pkgname=ac-offline
_gitname=ac-offline
pkgver=0.1.3
pkgrel=1
pkgdesc="Power saving parameters while on battery"
arch=(any)
url="http://github.com/aesiris/${_gitname}"
license=('GPL')
depends=(hdparm)
makedepends=(git)
source=("git://github.com/aesiris/${_gitname}#tag=v${pkgver}")
md5sums=(SKIP)

package() {
	cd "$srcdir/$_gitname"
	install -Dm 750 ac-offline "$pkgdir"/usr/bin/ac-offline
	install -D ac-offline.service "$pkgdir"/usr/lib/systemd/system/ac-offline.service
	install -D 50-powersave.rules "$pkgdir"/usr/lib/udev/rules.d/50-powersave.rules
}
