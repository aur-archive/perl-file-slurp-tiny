# CPAN Name  : File-Slurp-Tiny
# Submitter  : SIGTERM
# Maintainer : SIGTERM

pkgname='perl-file-slurp-tiny'
pkgver='0.003'
pkgrel='2'
pkgdesc="A simple, sane and efficient file slurper"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=0')
makedepends=()
url='http://search.cpan.org/dist/File-Slurp-Tiny'
source=('http://search.cpan.org/CPAN/authors/id/L/LE/LEONT/File-Slurp-Tiny-0.003.tar.gz')
md5sums=('b3c1c485b5bc40f7e94acfd983d7a871')
sha512sums=('28ad2e9d0030ce66ffa133aab403585d3ad42336d2e74e2dc5ed76976f4a2824cab5193b6fcb480cb8fc847887657242615b7fde2069df966097bfa2da2788ae')

build() {
  cd "$srcdir/File-Slurp-Tiny-0.003"
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

check() {
  cd "$srcdir/File-Slurp-Tiny-0.003"
  PERL_MM_USE_DEFAULT=1
  make test
}

package() {
  cd "$srcdir/File-Slurp-Tiny-0.003"
  make install DESTDIR="$pkgdir"
  find "$pkgdir" -name '.packlist' -o -name '*.pod' -delete
}
