# Maintainer: kaptoxic
# Contributor: Lockheed <qwrules@gmail.com>
# Contributor: Fenrihr <fmvm483@gmail.com>

pkgname=rainlendar-pro
pkgver=2.18.0
pkgrel=1
pkgdesc="A desktop Calendar, ToDo list and Event list"
arch=('x86_64')
url="http://www.rainlendar.net/"
license=('custom')
depends=(
    'cairo'
    'libsm'
    'expat>=1.95.8'
    'gtk2>=2.12.0'
    #'libstdc++5' # not needed
    #'libpng12' # not needed
    'openssl'
    #'librtmp0' # not needed
    'libcanberra'
    
    # requirements on the old enchant library
    #'enchant1.6' # not needed
    #'webkitgtk2' # not needed
    
    # libidn won't cut it
    #'libidn11' # not needed
)
provides=('rainlendar2')
conflicts=('rainlendar-beta' 'rainlendar-beta-unstable' 'rainlendar-lite')

source=(http://www.rainlendar.net/download/Rainlendar-Pro-$pkgver-amd64.tar.bz2)
sha256sums=('af300f0a772dc0c38b9a5b3f73c3b04e679159eec69bc6baf3d345349f1b6e12')

package() {
  cd ${srcdir}
  
  install -d "${pkgdir}"/{opt,usr/bin,usr/share/licenses/${pkgname}}

  cp -R ${srcdir}/rainlendar2 ${pkgdir}/opt
  ln -s /opt/rainlendar2/rainlendar2 ${pkgdir}/usr/bin/rainlendar
  ln -s /opt/rainlendar2/License.txt ${pkgdir}/usr/share/licenses/$pkgname/LICENSE
}

