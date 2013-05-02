# Maintainer: aesiris

pkgname=ac-offline
pkgver=0.1
pkgrel=1
pkgdesc="Power saving parameters while on battery"
arch=(any)
url="http://github.com/aesiris/${_pkgname}"
license=('GPL')
depends=(hdparm)
source=("git://github.com/aesiris/${_pkgname}#tag=${pkgver}")
md5sums=(SKIP)

package() {
	install -m 750 ac-offline "$pkgdir"/usr/bin/ac-offline
	install ac-offline.service "$pkgdir"/usr/lib/systemd/system/ac-offline.service
	install 50-powersave.rules "$pkgdir"/usr/lib/udev/rules.d/50-powersave.rules
}
