# Maintainer: Braytac
pkgname=opera-11.62-x86_64
_bigrelease=11.62
_buildver=1305
_randomizer=24069
pkgver=${_bigrelease}_${_buildver}
pkgrel=1
pkgdesc="A fast and secure web browser and Internet suite. Development version."
url="http://www.opera.com/browser/"
depends=('gcc-libs' 'libxt' 'freetype2' 'libxext')
provides=('opera')
optdepends=('gtk2: GTK integration'
	    'kdebase-runtime: KDE4 integration'
	    'gstreamer0.10-base-plugins: HTML5 open codecs support'
	    'gstreamer0.10-good: HTML5 open codecs support'
	    'gstreamer0.10-ffmpeg: HTML5 not so open codecs support'
	    'gstreamer0.10-bad-plugins: HTML5 not so open codecs support')
conflicts=('opera-116' 'opera-rc' 'opera-beta' 'opera-devel')
replaces=('opera' 'opera-116' 'opera-rc' 'opera-beta' 'opera-devel')
install=opera-11.62.install
options=(!strip !zipman)
license=('custom:opera')
arch=('x86_64')
_arch=x86_64
source=(http://snapshot.opera.com/unix/${_randomizer}_${_bigrelease}-1304/opera-${_bigrelease}-${_buildver}.${_arch}.linux.tar.xz)
md5sums=('ae0bb96939e3fe5d28f41ba1f4ca3311')

package() {
	opera-${_bigrelease}-${_buildver}.${_arch}.linux/install --prefix /usr --name opera --repackage "${pkgdir}"/usr
	install -D -m 644 "${pkgdir}"/usr/share/opera/defaults/license.txt "${pkgdir}"/usr/share/licenses/opera/license.txt
}

