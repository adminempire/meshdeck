pkgname=meshdeck
pkgver=2.04
groups=('blackarchlinux' 'blackarchlinux-drone' 'blackarchlinux-meta-thedeck')
pkgrel=4
pkgdesc="An addon to The Deck which allows multiple devices running The Deck to communicate via 802.15.4 Xbee and/or \
ZigBee mesh networking.  This allows coordinated attacks to be performed. A centralized command console is used to coordinate with the drones."
arch=('armv6h' 'armv7h')
# Change to github url
url='http://sourceforge.net/projects/thedeck/'
license=('creative-commons')
depends=('python-xbee')
# Change to pull from github repo
source=("meshdeck::git+https://github.com/adminempire/meshdeck.git")
md5sums=('SKIP')

# Leaving commented for now making sure test on p3 are OK
#prepare() {
#  cd "$srcdir/code"
#  sed -i 's|#!/usr/bin/python|#!/usr/bin/python2|' "$srcdir/code/meshdeck.py"
#}

package() {
  cd ${srcdir}/meshdeck/code
  install -d ${pkgdir}/usr/bin
  install -Dm744 meshdeck.py ${pkgdir}/usr/bin
  install -Dm644 meshdeckd.service ${pkgdir}/usr/lib/systemd/system/meshdeckd.service

}