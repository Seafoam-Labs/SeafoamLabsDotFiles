# Maintainer: Zoey Bauer <zoey.erin.bauer@gmail.com>
# Maintainer: Caroline Snyder <hirpeng@gmail.com>
pkgname=seafoamlabs-dotfiles
pkgver=1.0.0
pkgrel=1
pkgdesc="Seafoam Labs Noctalia colorschemes and GTK themes"
arch=('any')
url="https://github.com/Seafoam-Labs/SeafoamLabsDotFiles"
license=('MIT')
depends=()
install=seafoamlabs-dotfiles.install
source=("git+https://github.com/Seafoam-Labs/SeafoamLabsDotFiles.git")
sha256sums=('SKIP')

package() {
    cd "$srcdir/SeafoamLabsDotFiles"

    install -Dm644 \
        ".config/noctalia/colorschemes/SeafoamLabs/SeafoamLabs.json" \
        "$pkgdir/usr/share/seafoamlabs-dotfiles/colorschemes/SeafoamLabs/SeafoamLabs.json"

    install -Dm644 \
        ".config/noctalia/colorschemes/SeafoamLabs AMOLED/SeafoamLabs AMOLED.json" \
        "$pkgdir/usr/share/seafoamlabs-dotfiles/colorschemes/SeafoamLabs AMOLED/SeafoamLabs AMOLED.json"

    mkdir -p "$pkgdir/usr/share/seafoamlabs-dotfiles/themes"
    cp -r .local/share/themes/SeafoamLabs "$pkgdir/usr/share/seafoamlabs-dotfiles/themes/"
    cp -r .local/share/themes/SeafoamLabs-AMOLED "$pkgdir/usr/share/seafoamlabs-dotfiles/themes/"
}
