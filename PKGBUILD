# Maintainer: Kolja Dummann <kolja.dummann@logv.ws>

pkgname=jetbrains-mps-eap
pkgver=3.0.129_189
pkgrel=1
pkgdesc="JetBrains Meta Programming System EAP"
arch=('any')
url="http://www.jetbrains.com/mps/index.html"
license=('custom: MPS license agreement')
depends=('jdk6')
makedepends=('')
optdepends=()
source=("http://download.jetbrains.com/mps/30/MPS-3.0-EAP-129.189.tar.gz")
md5sums=('40d9a876bb789102b9796b31df1b0379')

build() {
    cd "${srcdir}"
    echo "#!/bin/sh" > mps
    echo "JDK_HOME=/opt/java6 /opt/jetbrains-mps-eap/mps.sh" >> mps
}

package() {
    install -d "${pkgdir}/opt/"
    mv "${srcdir}/MPS 3.0/" "${pkgdir}/opt/jetbrains-mps-eap"
    install -m 755 -D "${srcdir}/mps" "${pkgdir}/usr/bin/mps-eap"
}
