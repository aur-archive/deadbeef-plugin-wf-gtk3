# Author: Jan D. Behrens <zykure@web.de>
# Maintainer: Jan D. Behrens <zykure@web.de>

pkgname=deadbeef-plugin-wf-gtk3
pkgver=20141101
pkgrel=1
pkgdesc="A waveform display plugin for the DeaDBeeF audio player"
arch=('any')
url="http://sourceforge.net/projects/deadbeef-wf/"
license=(GPL)
depends=('deadbeef>=0.6', gtk3)
backup=()
source=(http://downloads.sourceforge.net/project/deadbeef-wf/master/deadbeef-wf_20141101_src.tar.gz)
md5sums=('a3038dd5defb5a6bd30047ab18bbed33')
sha1sums=('7a36eead6f3c886c2fe4e8270e34bd41d8febbe1')
sha256sums=('92141289eaec0e4817bbd5ceb3f39dab7c1597b146167fea29eea0754693a91e')

build() {
  cd $srcdir/deadbeef-wf-devel
  ./configure --prefix=/usr --disable-gtk2
  make
}

package() {
  cd $srcdir/deadbeef-wf-devel
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
