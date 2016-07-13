# Maintainer: Joe Julian <me@joejulian.name>

pkgname=asciidoctor-diagram
pkgver=1.5.1
pkgrel=1
pkgdesc='Asciidoctor diagram extension, with support for PlantUML, Graphviz and ditaa.'
arch=(any)
url='http://asciidoctor.org'
license=(MIT)
depends=(ruby)
options=(!emptydirs)
source=("https://rubygems.org/downloads/${pkgname}-${pkgver}.gem")
noextract=($pkgname-$pkgver.gem)
sha1sums=('34f7bea8ae95a482bea62d8751bd51a1304e05aa')

package() {
    local _gemdir="$(ruby -e 'puts Gem.default_dir')"
    gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" "$pkgname-$pkgver.gem"
    install -D -m644 "$pkgdir/$_gemdir/gems/$pkgname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
    rm "$pkgdir/$_gemdir/cache/$pkgname-$pkgver.gem"
}
