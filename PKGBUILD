# $Id: PKGBUILD 81210 2012-12-13 05:55:07Z idevolder $
# Maintainer: BlackEagle < ike DOT devolder AT gmail DOT com >
# Contributor: Bram Schoenmakers <me@bramschoenmakers.nl>
pkgname=closure-compiler
pkgver=20140407
pkgrel=1
pkgdesc="Performs checking, instrumentation and optimizations on Javascript code."
arch=('any')
url="http://code.google.com/closure"
license=('APACHE')
depends=('java-runtime')
source=("http://dl.google.com/$pkgname/compiler-$pkgver.tar.gz")

package() {
	cd $srcdir

	install -m755 -D compiler.jar "$pkgdir/usr/share/java/closure-compiler/closure-compiler.jar"
	mkdir $pkgdir/usr/bin
	echo '#!/bin/sh
	"$JAVA_HOME/bin/java" -jar /usr/share/java/closure-compiler/closure-compiler.jar $@' > "$pkgdir/usr/bin/closure"
	chmod +x "$pkgdir/usr/bin/closure"
}

sha256sums=('ee640b598e7ead8a90b15702afffcda6626a07a6e5f9032623fe6be48b8ca933')
