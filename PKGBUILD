# Maintainer:  kor44 http://opendesktop.org>

pkgname=regexptester
_name=RegExpTester
pkgver=0.2a
pkgrel=2
pkgdesc="A fast test QRegExp."
arch=('i686' 'x86_64')
url="http://qt-apps.org/content/show.php/Photo?content=147453"
license='GPL'
depends=('qt4')
makedepends=('')
source=("http://opendesktop.org/CONTENT/content-files/150094-RegExpTester_v${pkgver}_src.zip")

md5sums=('25d91b6187e815492f0c324e1834f2d9')

build() {
#  cd $srcdir/150094-$_name$pkgver

   # Build
  qmake-qt4
  sed -i '15s|-pipe|-pipe -fpermissive|g' $srcdir/Makefile
  make 
  #make DESTDIR=$pkgdir install
  #install -dm 755 $pkgdir/usr/bin
  #cp -r ${srcdir}/RegExpTester ${startdir}/pkg/usr/bin

}

package() {
  install -dm 755 $pkgdir/usr/bin
  cp -r ${srcdir}/RegExpTester $pkgdir/usr/bin
}
