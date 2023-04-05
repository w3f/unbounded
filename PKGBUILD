# Maintainer: hitchhooker <contact@expectchaos.com>
pkgname=unbounded-fonts
pkgver=1.0
pkgrel=1
pkgdesc="Unbounded font family (TTF, WOFF, and Variable formats)"
arch=('any')
url="https://github.com/w3f/unbounded"
license=('custom')
depends=('fontconfig' 'xorg-font-util')
source=("https://github.com/w3f/unbounded/archive/refs/heads/main.zip")
sha256sums=('SKIP')

package() {
	cd "$srcdir/unbounded-main"

	# Install TTF fonts
	install -dm755 "${pkgdir}/usr/share/fonts/TTF"
	install -m644 TTF/*.ttf "${pkgdir}/usr/share/fonts/TTF/"

	# Install WOFF fonts
	install -dm755 "${pkgdir}/usr/share/fonts/WOFF"
	install -m644 WOFF/*.woff2 "${pkgdir}/usr/share/fonts/WOFF/"

	# Install Variable fonts
	install -dm755 "${pkgdir}/usr/share/fonts/Variable"
	install -m644 Variable/Unbounded-Variable.ttf "${pkgdir}/usr/share/fonts/Variable/"

	# Install license
	install -dm755 "${pkgdir}/usr/share/licenses/${pkgname}"
	install -m644 OFL.txt "${pkgdir}/usr/share/licenses/${pkgname}/"
}
