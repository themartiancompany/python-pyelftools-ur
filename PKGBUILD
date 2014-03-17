# Maintainer : Rémy Oudompheng <remy@archlinux.org>

pkgname=python-pyelftools
_pypiname=pyelftools
pkgver=0.21
pkgrel=2
pkgdesc="Python library for analyzing ELF files and DWARF debugging information"
arch=('any')
url="http://pypi.python.org/pypi/pyelftools"
license=('custom')
depends=('python')
source=("http://pypi.python.org/packages/source/p/${_pypiname}/${_pypiname}-${pkgver}.tar.gz")
md5sums=("fe1039193675cb9d0ddf60d1431fbea3")

build() {
  cd ${srcdir}/${_pypiname}-${pkgver}
  python setup.py build
}

check() {
  cd ${srcdir}/${_pypiname}-${pkgver}
  python test/run_all_unittests.py
}

package() {
  cd ${srcdir}/${_pypiname}-${pkgver}
  python setup.py install --root=${pkgdir}
  install -D -m 644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}

