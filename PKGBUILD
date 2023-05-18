# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=inputcontext-gtk
pkgver=0.99.2
pkgrel=2
pkgdesc="The GTK+ input context for Maliit."
arch=('x86_64' 'aarch64')
url="https://github.com/maliit/inputcontext-gtk"
license=('LGPL-2.1-only')
depends=('maliit-framework')
makedepends=('qt5-tools' 'gtk2' 'gtk3' 'cmake' 'git')
source=('inputcontext-gtk::git+https://github.com/maliit/inputcontext-gtk')
sha256sums=('SKIP')

build() {
    cmake \
        -B "inputcontext-gtk/build" \
        -S "inputcontext-gtk" \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make -C "inputcontext-gtk/build" all
}

package() {
    make -C "${srcdir}/inputcontext-gtk/build" DESTDIR="$pkgdir" install
}
