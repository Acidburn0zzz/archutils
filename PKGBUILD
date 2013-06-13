# Maintainer: Sébastien Luttringer

pkgname=archutils-git
pkgver=$(date +%Y.%m.%d)
pkgrel=1
pkgdesc='Seblu Archlinux Utils'
arch=('any')
url='https://github.com/seblu/archutils'
license=('GPL2')
depends=('python' 'bash')

package() {
  cd "$startdir"
  install -dm755 "$pkgdir"/usr/{share/licenses/$pkgname,bin}
  # install legal stuff
  install -m644 COPYRIGHT LICENSE "$pkgdir/usr/share/licenses/$pkgname"
  # install binaries
  install -m755 atc aurdown go2chroot	addpkg sign archbuild-dl pkgbuild2json \
    tmpmakepkg reinstallpkgs restart-updated-service "$pkgdir/usr/bin"
}

# vim:set ts=2 sw=2 et:
