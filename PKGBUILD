# Maintainer: Michael Weichert <mweichert@gmail.com>
pkgname=membase-server
pkgver=1.7.0
pkgrel=1
pkgdesc="Memcached-compatible distributed, key-value database management system optimized for storing data behind interactive web applications"
url="http://www.membase.org"
arch=("x86_64")
license=("APACHE")
depends=("icu" "erlang" "python2" "libevent" "spidermonkey" "curl" "check" "sqlite3" "glib2" "cyrus-sasl" "ncurses")
conflicts=("memcached")
source=("http://files.couchbase.com/source/membase-server_src-${pkgver}.tar.gz")
md5sums=("c933fffea299d00e43b002cb65738663")

build() {
	cd "${srcdir}/${pkgname}_src"
  make
}

package() {
  cd "${srcdir}/${pkgname}_src"
  make DESTDIR=${pkgdir} install
  #cp -rf "./install" "${pkgdir}"
}

