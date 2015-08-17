# Maintainer: speps <speps at aur dot archlinux dot org>

pkgname=sipclients
pkgver=1.0.0
pkgrel=1
pkgdesc="SIP SIMPLE Command Line Clients"
arch=('any')
url="http://www.icanblink.com"
license=('custom:MIT')
depends=('avahi' 'python2-sipsimple')
source=("http://download.ag-projects.com/SipClient/$pkgname-$pkgver.tar.gz")
md5sums=('c97e255bfea2c013eb394a3b672d0cb4')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python2 setup.py install --root="$pkgdir/"

  # license
  install -Dm644 LICENSE \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
