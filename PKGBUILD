pkgname=meshdeck
pkgver=2.04
groups=('blackarchlinux' 'blackarchlinux-drone' 'blackarchlinux-meta-thedeck')
pkgrel=4
pkgdesc="MeshDeck which is an addon to The Deck which allows multiple devices running The Deck to communicate via 802.15.4 Xbee and/or \
ZigBee mesh networking.  This allows coordinated attacks to be performed. A centralized command console is used to coordinate with the drones."
arch=('armv6h' 'armv7h')
url='http://sourceforge.net/projects/thedeck/'
license=(' ')
depends=('python-xbee')
source=("http://downloads.sourceforge.net/sourceforge/thedeck/meshdeck.tar.gz"
        "meshdeckd.service")
md5sums=('561acddff336d0408ad7bf663fe274d7')

prepare() {
  cd "$srcdir/code"
  sed -i 's|#!/usr/bin/python|#!/usr/bin/python2|' "$srcdir/code/meshdeck.py"
}

package() {
  cd ${srcdir}/code

  install -d ${pkgdir}/usr/bin

  install -Dm744 meshdeck.py ${pkgdir}/usr/bin
  install -Dm644 meshdeckd.service ${pkgdir}/usr/lib/systemd/system/meshdeckd.service

}