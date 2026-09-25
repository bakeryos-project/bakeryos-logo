pkgname=bakeryos-logo
pkgver=1.1.1
pkgrel=1
pkgdesc="Logo of BakeryOS"
arch=('any')
url="https://github.com/bakeryos-project/bakeryos-logo"
license=("GPL-3.0-or-later")
source=()
sha256sums=()
options=(!debug !strip)
provides=('bakeryos-logo')
conflicts=('bakeryos-logo')
install=bakeryos-logo.install

package() {
    install -d "${pkgdir}/usr/share"
    install -d "${pkgdir}/usr/share/bakeryos/logo"
    install -d "${pkgdir}/usr/share/pixmaps"
    for img in "${srcdir}/bakeryos/logo/"*; do
        if [ -f "$img" ]; then
        install -Dm644 "$img" "${pkgdir}/usr/share/bakeryos/logo/$(basename "$img")"
        fi
    done
    install -Dm644 "${startdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

