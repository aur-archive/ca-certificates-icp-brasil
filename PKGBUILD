# Maintainer: Aristides Caldeira <ari@laumi.org>
pkgname=ca-certificates-icp-brasil
pkgver=20140616
pkgrel=1
pkgdesc="CA-certificates from Brazil's government's certificate chain"
arch=('any')
url="http://www.iti.gov.br/twiki/bin/view/Certificacao/RepositoriodaACRaiz"
license=('GPL')
depends=('ca-certificates')
makedepends=('unzip')
install='ca-certificates-icp-brasil.install'
source=(
    'http://acraiz.icpbrasil.gov.br/credenciadas/CertificadosAC-ICP-Brasil/ACcompactado.zip'
    )
#
# SHA512 taken from here:
# http://acraiz.icpbrasil.gov.br/credenciadas/CertificadosAC-ICP-Brasil/hashsha512.txt
#
sha512sums=(
    '1ca7ecbc2d4999ea079edcaa1057e96dcb4346507cace7d5c5b58cddf833c666c0f7995dc7b359793ffe8fb7996097f4c356448098c83681df584ebf40cd3f97'
    )

package() {
  cd "$srcdir"
  chmod a-x *.crt
  mkdir -p "$pkgdir/usr/local/share/ca-certificates/brasil.gov.br"
  cp *.crt "$pkgdir/usr/local/share/ca-certificates/brasil.gov.br/"
}
