# $Id$
# Maintainer: Juan Cañete <jcazor@komlog.org>

pkgname=('python-cassandra')
pkgver=3.4.1
pkgrel=1
pkgdesc='Python driver for Cassandra'
arch=('i686' 'x86_64')
url='http://github.com/datastax/python-driver'
license=('Apache')
makedepends=('python-setuptools' 'git' 'gcc' 'libevdev')
checkdepends=()
#checkdepends=('python-nose' 'python-mock' 'python-yaml' 'python-pytz' 'python-sure')
source=("git+https://github.com/datastax/python-driver.git#tag=$pkgver")
md5sums=('SKIP')

build() {
  cd python-driver
  python setup.py build

}

#check() {
    #cd python-driver
    #python setup.py nosetests -w tests/unit/
#}

package_python-cassandra() {
  depends=('python' 'python-six')
  optdepends=('lz4: for compression support in cassandra 2.0+'
              'snappy: for compression support in cassandra 1.2+'
              'libevent: alternative to python asyncore for a better performance event loop')

  cd python-driver
  python setup.py install --root="${pkgdir}" --optimize=1
}
