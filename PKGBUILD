pkgname=shntool
pkgver=3.0.10
pkgrel=3
pkgdesc="A multi-purpose WAVE data processing and reporting utility"
arch=('x86_64')
url="http://www.etree.org/shnutils/shntool/"
license=('GPL')
options=(!emptydirs)
depends=('glibc')
optdepends=('mac: Monkey Audio support')
source=("http://www.etree.org/shnutils/shntool/dist/src/${pkgname}-${pkgver}.tar.gz")
md5sums=('5d41f8f42c3c15e3145a7a43539c3eae')
sha1sums=('7a2bc8801e180cf582f0e39775603582e35d50d2')

build() {
	cd "${srcdir}"/${pkgname}-${pkgver}
	./configure --prefix=/usr
	make
}
package() {
	cd "${srcdir}"/${pkgname}-${pkgver}
	make DESTDIR="${pkgdir}" install
}

# vim:set ts=2 sw=2 et:
