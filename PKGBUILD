# Maintainer: Vadim Ushakov <igeekless@gmail.com>

pkgname=wmctrl-geekless-git
pkgver=20140210
pkgrel=1
conflicts=('wmctrl' 'wmctrl-with-undecorated-support')
provides=('wmctrl=1.07')
pkgdesc="wmctrl is a tool to control your EWMH compliant window manager from command line. This version includes support for Openbox's undecorated flag, sorting of the window list in stacking order and ability to iconify (minimize) windows."
url="http://make-linux.org/"
arch=('i686' 'x86_64')
license=('GPL')
depends=(libxmu glib2)

source=('git+git://make-linux.org/tools/wmctrl.git')
md5sums=('SKIP')

_gitname="wmctrl"

pkgver() {
  date +%Y%m%d
}

build() {
    cd "${_gitname}"
    ./configure --prefix=/usr --mandir=/usr/share/man
    make
}

package() {
    cd "${_gitname}"
    make DESTDIR="$pkgdir/" install
}
