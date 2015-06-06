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
  install -dm755 "$pkgdir"/usr/{share/licenses/$pkgname,bin,lib/munin/plugins}
  # install legal stuff
  install -m644 COPYRIGHT LICENSE "$pkgdir/usr/share/licenses/$pkgname"
  # install binaries
  install -m755 atc aurdown go2chroot	addpkg sign getpkg pkgbuild2json \
    tmpmakepkg reinstallpkgs checkservices bindeps archlinux-update reexec \
    "$pkgdir/usr/bin"
  # install munin stuff
  install -m755 archlinux-{pacfiles,packages} "$pkgdir/usr/lib/munin/plugins"
  # add shortcut, because i'm lazy
  ln -s checkservices "$pkgdir/usr/bin/cs"
}

# vim:set ts=2 sw=2 et:
