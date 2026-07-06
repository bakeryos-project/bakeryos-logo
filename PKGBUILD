pkgname=bakeryos-logo
pkgver=1.0.0
pkgrel=1
pkgdesc="Logo of BakeryOS"
arch=('any')
url="https://gitlab.com/bakeryos/bakeryos-logo"
license=("GPL-3.0-or-later")
source=("LICENSE" "README.md")
sha256sums=('SKIP' 'SKIP')

pkgver() {
    git describe --long --tags --always | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

prepare() {
    cp -r ../usr "${srcdir}/"
}

package() {
    install -d "${pkgdir}/usr"
    cp -r usr/* "${pkgdir}/usr/"

    install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

