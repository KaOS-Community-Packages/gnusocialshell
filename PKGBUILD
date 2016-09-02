pkgname=gnusocialshell
_pkgname=GnuSocialShell
pkgver=1.0
pkgrel=1
pkgdesc="A simple GnuSocial client for UNIX-like Operating Systems"
arch=('x86_64')
url="http://gnusocialshell.amayaos.com/index.html"
license=('GPL')
depends=('curl')
install=gnusocialshell.install
source=("http://gnusocialshell.amayaos.com/downloads/${_pkgname}-${pkgver}.tar.gz"
        "config_directory.patch"
        "gnusocialshell.install")
md5sums=('7bf2d3e1b046fe304423ac66dd7831ed'
         '4c0a585f8c0d9e311bfbfd83ad13bdf5'
         'b404346ff882560187ad06a5444d0e4f')

prepare(){
cd "${_pkgname}-${pkgver}"

patch -p1 -i $srcdir/config_directory.patch

}

package(){
cd "${_pkgname}-${pkgver}"

make DESTDIR="$pkgdir" install

}
