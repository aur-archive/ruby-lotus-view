# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Alireza Savand <alireza.savand@gmail.com>

_gemname=lotus-view
pkgname=ruby-$_gemname
pkgver=0.2.0
pkgrel=1
pkgdesc='View layer for Lotus, with a separation between views and templates'
arch=(any)
url='http://lotusrb.org'
license=(MIT)
depends=(ruby ruby-tilt ruby-lotus-utils)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('dfb4abd57f086518295ada4047b5acce1319d075')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
