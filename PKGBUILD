# Maintainer: Brandon Invergo <brandon@invergo.net>
pkgname=guile2-colorized-git
_gitname=guile-colorized
pkgver=9.535b314
pkgrel=1
pkgdesc="A colorized REPL for GNU Guile 2"
arch=('any')
url="https://github.com/NalaGinrut/guile-colorized"
license=('GPL3')
depends=('guile')
makedepends=('git')
install=${pkgname}.install
source=('git://github.com/NalaGinrut/guile-colorized.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd "$srcdir/$_gitname"
  mkdir -p "$pkgdir/usr/share/guile/site/ice-9"
  install -m644 ice-9/colorized.scm "$pkgdir/usr/share/guile/site/ice-9/colorized.scm"
}

# vim:set ts=2 sw=2 et:
