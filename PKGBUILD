# Maintainer: lilydjwg <lilydjwg@gmail.com>

_gitname=greenlet
pkgname=python-greenlet-git
pkgver=0.4.2.11_g07b799d
pkgrel=1
pkgdesc="Lightweight in-process concurrent programming"
arch=('i686' 'x86_64')
url="https://github.com/python-greenlet/greenlet"
license=('MIT')
depends=('python')
makedepends=('git')
conflicts=(python-greenlet python-greenlet-hg)
replaces=(python-greenlet-hg)
provides=(python-greenlet=0.4.0)
source=('git://github.com/python-greenlet/greenlet.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git describe --tags | sed 's/-/./;s/-/_/g'
}

package() {
  cd "$srcdir/$_gitname"
  python3 setup.py install --root="$pkgdir/" --optimize=1
}

