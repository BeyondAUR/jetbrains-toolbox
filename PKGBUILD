# Maintainer: Frederik Schwan <freswa at archlinux dot org>

pkgname=jetbrains-toolbox
pkgver=3.9.1.89198
pkgrel=1
pkgdesc='Manage all your JetBrains Projects and Tools'
arch=('x86_64' 'i686')
url='https://www.jetbrains.com/toolbox/'
license=('custom:jetbrains')
depends=(
  glib2
  libxslt
  libxss
  nss
  org.freedesktop.secrets
  xcb-util-keysyms
  xdg-utils
)
options=('!strip' '!debug')
source=("https://download.jetbrains.com/toolbox/${pkgname}-${pkgver}.tar.gz"
        jetbrains-toolbox.desktop
        icon.svg
        LICENSE)
b2sums=('092dbff91e1e660f45bed99c2c26c582165cc1ed07bfccefbe9420c9f3c9fd715bca4c3f85f19f3b91b60d524a03c43ca9011b60c08c4708d9b552dbc22bdbd5'
        'f62cacc9eeda4e2c96e25bc97b7e353db78ad7785ddbbf8eed1ca63328396c115385b608f597060bc2070c6934e11d24c6fc178966d790546b076c2b27eba577'
        '4b10487746fcb7f328cbdc8b17432f82618c5695baee4ef30e23ff3c4d4b6096daf2fcdfb4c1e2e179e2e61f68bbd88104e5df5a2e6e969aad0a68a75cfff496'
        'dadaf0e67b598aa7a7a4bf8644943a7ee8ebf4412abb17cd307f5989e36caf9d0db529a0e717a9df5d9537b10c4b13e814b955ada6f0d445913c812b63804e77')

package() {
  install -dm755 "${pkgdir}"/usr/bin/ "${pkgdir}"/opt/"${pkgname}"
  install -Dm644 "${srcdir}"/${pkgname}.desktop "${pkgdir}"/usr/share/applications/${pkgname}.desktop
  install -Dm644 "${srcdir}"/icon.svg "${pkgdir}"/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg
  install -Dm644 LICENSE "${pkgdir}"/usr/share/licenses/${pkgname}/LICENSE.txt

  cp -ar "${srcdir}"/"${pkgname}-${pkgver}"/bin/* "${pkgdir}/opt/${pkgname}/"
  ln -s /opt/"${pkgname}"/"${pkgname}" "${pkgdir}"/usr/bin/${pkgname}
}
