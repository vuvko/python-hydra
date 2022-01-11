# Maintainer: Harley Wiltzer <harleyw@hotmail.com>
# Contributor: Andrei Shadrikov <notvuvko@gmail.com>
pkgname='python-hydra'
_pkgname=${pkgname/python-/}
pkgver='1.1.1'
pkgrel=1
_project="$_pkgname-$pkgver"
epoch=
pkgdesc='A framework for elegantly configuring complex applications'
arch=('any')
url='https://hydra.cc'
license=('MIT')
depends=('python-omegaconf>=2.0')
makedepends=(python-setuptools)
provides=('python-hydra')
source=("https://github.com/facebookresearch/hydra/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('03840c5192d47c3b0a4cf57e1815f8626d36f2fed81efed59202f6bd93ac822c')

build() {
  cd "$srcdir/$_project"
  python setup.py build
}

package() {
  cd "$srcdir/$_project"
  python setup.py install --root "$pkgdir" --skip-build
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
