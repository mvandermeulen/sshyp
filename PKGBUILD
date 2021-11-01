# Maintainer: Randall Winkhart <idgr at tutanota dot com>
# The source package is no longer recieving updates past this version.

pkgname=rpass
pkgver=2021.11.01.mr5.1
pkgrel=1
pkgdesc='An rsync-based password manager and alternative to GNU pass'
url='https://github.com/rwinkhart/sshyp'
arch=('x86_64' 'aarch64')
license=('GPL3')
depends=( python gnupg openssh rsync nano xclip wl-clipboard)

source_x86_64=('https://github.com/rwinkhart/sshyp/releases/download/v2021.11.01.mr5.1/rpass-2021.11.01.mr5.1.tar.xz')
source_aarch64=('https://github.com/rwinkhart/sshyp/releases/download/v2021.11.01.mr5.1/rpass-2021.11.01.mr5.1.tar.xz')
sha512sums_x86_64=('bf0c958721de1a13ca814d91bf74cbaaebe458198cba14b96b95fb1eeb72a1b901c8d3d00ea4c18ddff0d10d9ef6504a17a4caa345917412108df4787add61fd')
sha512sums_aarch64=('bf0c958721de1a13ca814d91bf74cbaaebe458198cba14b96b95fb1eeb72a1b901c8d3d00ea4c18ddff0d10d9ef6504a17a4caa345917412108df4787add61fd')

package() {

	tar xf rpass-"$pkgver".tar.xz -C "${pkgdir}"
	chown -R "$USER" ${pkgdir}/var/lib/rpass

}
