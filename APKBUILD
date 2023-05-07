
pkgname=firmware-leeco-s2-mainline
pkgver=5
pkgrel=0
pkgdesc="Firmware for LeEco Le2"
url="https://github.com/Kiciuk/proprietary_firmware_s2"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit="e156b31c2a7096c00e45a1dff76f1200b82ad83d"
source="https://github.com/Kiciuk/proprietary_firmware_s2/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_s2-$_commit"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	# modem firmware
	install -Dm644 modem/mba.mbn -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem.* -t "$pkgdir/$_fwdir"

	# video firmware
	install -Dm644 apnhlos/venus* -t "$pkgdir/$_fwdir"

	# WiFi/BT firmware
	install -Dm644 apnhlos/wcnss.* -t "$pkgdir/$_fwdir"
	install -Dm644 firmware/wlan/prima/WCNSS_qcom_wlan_nv.bin -t "$pkgdir/$_fwdir"/wlan/prima

	# ADSP firmware
	install -Dm644 modem/adsp.* -t "$pkgdir/$_fwdir"

	# GPU firmware
	install -Dm644 apnhlos/a530* -t "$pkgdir/$_fwdir"
}

sha512sums="
76451e238bf8d59ae38421d345265982805187122fb037e1e60dac2f368b89a035b9b53dc246819613b1f104b043429406f2ba55f2fb416d8c44c3a75376d443  e156b31c2a7096c00e45a1dff76f1200b82ad83d.zip
"
