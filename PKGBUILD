# Maintainer: Frederik Schwan <freswa at archlinux dot org>

pkgname=jetbrains-toolbox
pkgver=2.6.0.40632
pkgrel=1
pkgdesc='Manage all your JetBrains Projects and Tools'
arch=('x86_64' 'i686')
url='https://www.jetbrains.com/toolbox/'
license=('custom:jetbrains')
depends=('fuse' 'glib2' 'libxslt' 'libxss' 'xcb-util-keysyms' 'xdg-utils' 'nss')
optdepends=('xdg-utils: open URLs')
options=('!strip')
source=("https://download.jetbrains.com/toolbox/${pkgname}-${pkgver}.tar.gz"
        jetbrains-toolbox.desktop
        icon.svg
        LICENSE)
b2sums=('1492c2657f0203d3b26c3540e970d4afd7fa9183300f05485f94e4c60cba062a9d5ee5edd38777caf18f26081a5f6df629a9a73cdcbaad80ee29d75fee943116'
        'f62cacc9eeda4e2c96e25bc97b7e353db78ad7785ddbbf8eed1ca63328396c115385b608f597060bc2070c6934e11d24c6fc178966d790546b076c2b27eba577'
        '4b10487746fcb7f328cbdc8b17432f82618c5695baee4ef30e23ff3c4d4b6096daf2fcdfb4c1e2e179e2e61f68bbd88104e5df5a2e6e969aad0a68a75cfff496'
        'dadaf0e67b598aa7a7a4bf8644943a7ee8ebf4412abb17cd307f5989e36caf9d0db529a0e717a9df5d9537b10c4b13e814b955ada6f0d445913c812b63804e77')

package() {
  install -dm755 "${pkgdir}"/usr/bin/
  install -Dm644 "${srcdir}"/${pkgname}.desktop "${pkgdir}"/usr/share/applications/${pkgname}.desktop
  install -Dm644 "${srcdir}"/icon.svg "${pkgdir}"/usr/share/pixmaps/${pkgname}.svg
  install -Dm755 "${srcdir}"/${pkgname}-${pkgver}/${pkgname} "${pkgdir}"/usr/bin/${pkgname}
  install -Dm644 LICENSE "${pkgdir}"/usr/share/licenses/${pkgname}/LICENSE.txt
}
