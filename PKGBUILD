# Maintainer: Michael Weichert <mweichert@gmail.com>
pkgname=membase-server-community
pkgver=1.7.0
pkgrel=1
pkgdesc="Memcached-compatible distributed, key-value database management system optimized for storing data behind interactive web applications"
url="http://www.membase.org"
arch=("x86_64")
license=("APACHE")
depends=("erlang" "python2" "libevent" "curl")
conflicts=("memcached")
source=("http://files.couchbase.com/source/membase-server_src-${pkgver}.tar.gz")
md5sums=("c933fffea299d00e43b002cb65738663")

build() {
	cd "${srcdir}/membase-server_src"
  #./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var
  make
  make test
}

package() {
  cd "${srcdir}/membase-server_src"
  make DESTDIR=${pkgdir} install
}

