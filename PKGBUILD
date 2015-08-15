# Contributor: Rémy Oudompheng <remy@archlinux.org>

pkgname=gfan
pkgver=0.5
pkgrel=1
pkgdesc="A software package for computing Gröbner fans and tropical varieties"
arch=('i686' 'x86_64')
url="http://home.imf.au.dk/jensen/software/gfan/gfan.html"
license=('GPL')
depends=('cddlib')
source=("http://home.imf.au.dk/jensen/software/gfan/gfan${pkgver}.tar.gz" 'fix-build.patch')
md5sums=('2d76d1625e0766c57c2b3ece809c23c8'
         'e327ec23a3bdf20ce6c8711ab154db50')

build() {
  cd gfan$pkgver
  patch -p1 -i $srcdir/fix-build.patch
  make
}

package() {
  cd gfan$pkgver
  make PREFIX="$pkgdir"/usr install
}
