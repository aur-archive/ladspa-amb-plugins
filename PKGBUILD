# $Id$
# Maintainer: Arch Linux Pro Audio <dev@archaudio.org>
# Contributor: Bernardo Barros <bernardobarros@gmail.com>
# Contributor: Shinlun Hsieh <yngwiexx@yahoo.com.tw>
# Contributor: Wido <widomaker2k7@gmail.com>

pkgname=ladspa-amb-plugins
_pkgname=AMB-plugins
pkgver=0.8.1
pkgrel=2
pkgdesc="LADSPA plugins of various improved decoders"
arch=('i686' 'x86_64')
url="http://kokkinizita.linuxaudio.org/"
license=('GPL')
provides=('amb-plugins' 'ladspa-amb')
conflicts=('amb-plugins' 'ladspa-amb')

groups=('ladspa-plugins')

depends=('gcc-libs')
source=(http://kokkinizita.linuxaudio.org/linuxaudio/downloads/$_pkgname-$pkgver.tar.bz2)
md5sums=('496d8d2bf6036611b6b4aa7f56325a52')


build() {

  cd $srcdir/${_pkgname}-$pkgver
  make
}

package() {

  cd $srcdir/${_pkgname}-$pkgver
  install -d "$pkgdir/usr/lib/ladspa/"
  install -m 755 *.so "$pkgdir/usr/lib/ladspa/"
}
