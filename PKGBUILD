# Maintainer: Frederik Schwan <freswa at archlinux dot org>

pkgname=jetbrains-toolbox
pkgver=3.3.1.75249
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
source=("https://download-cdn.jetbrains.com/toolbox/${pkgname}-${pkgver}.tar.gz"
        jetbrains-toolbox.desktop
        icon.svg
        LICENSE)
b2sums=('ed18f9a96c732c603b4defc9a6ae45967dd47c45e43f6bcab349120494abbaf4ce7fa08c670fbe65c6448e487c68c6aff8f7a52a20436ad8bc76ff6bb6d886c3'
        'f62cacc9eeda4e2c96e25bc97b7e353db78ad7785ddbbf8eed1ca63328396c115385b608f597060bc2070c6934e11d24c6fc178966d790546b076c2b27eba577'
        '6690f2b0c97f634e41435c084166779c3900329722405f16cb2ce8c9c90a9b9d87b3d1a5aa1b1702858eb1949de5b266d3810994cf2e0093b9510d41ac914913'
        'dadaf0e67b598aa7a7a4bf8644943a7ee8ebf4412abb17cd307f5989e36caf9d0db529a0e717a9df5d9537b10c4b13e814b955ada6f0d445913c812b63804e77')

package() {
  install -dm755 "${pkgdir}"/usr/bin/ "${pkgdir}"/opt/"${pkgname}"
  install -Dm644 "${srcdir}"/${pkgname}.desktop "${pkgdir}"/usr/share/applications/${pkgname}.desktop
  install -Dm644 "${srcdir}"/icon.svg "${pkgdir}"/usr/share/icons/hicolor/scalable/${pkgname}.svg
  install -Dm644 LICENSE "${pkgdir}"/usr/share/licenses/${pkgname}/LICENSE.txt

  cp -ar "${srcdir}"/"${pkgname}-${pkgver}"/bin/* "${pkgdir}/opt/${pkgname}/"
  ln -s /opt/"${pkgname}"/"${pkgname}" "${pkgdir}"/usr/bin/${pkgname}
}
