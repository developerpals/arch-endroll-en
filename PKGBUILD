# This PKGBUILD is for my personal system, and will not be mantained.

pkgname=endroll-en
pkgver=2.01
pkgrel=1
pkgdesc='A regretful adventure RPG (English translation by vgperson)'
url='https://vgperson.com/games/endroll.htm'
arch=('any')
license=('Freeware')
depends=('easyrpg-player')
source=("https://vgperson.com/games/EndRoll201.zip"
        'ENDROLL'
        'ENDROLL.desktop')
sha512sums=(''
	    '66ef5da71a55fa15a8594948855c8d0ece7198cb6c4728d521823120c9e46b4ba7bbf52ceb63928b2af197c567de8550cc54b37108e75d9ad59b541d33aa2d35'
     	    '143f209f25bb4ff21ff59d67102f8030a318e15a2dcd4e0c4e1235ec305d6a12317a8e360de52a1bbda9ad197341b0d3468399b69b502d8d6369a50db00a82a1')

package() {
	(
		cd 'EndRoll201'

		mkdir -p "$pkgdir/usr/share/doc/ENDROLL"
		mv '- Game Hints' "$pkgdir/usr/share/doc/ENDROLL"
		mv '- On Bonus Content' "$pkgdir/usr/share/doc/ENDROLL"
		printf 'Note: the "How to Start" section is not relevant when using the endroll-en package.\n\n' > "$pkgdir/usr/share/doc/ENDROLL/'- END ROLL Readme'"
		cat '- END ROLL Readme' >> "$pkgdir/usr/share/doc/ENDROLL/'- END ROLL Readme'"
		rm -v !('Data')
		mv 'Data'/* .
	)

	install -Dm755 ENDROLL -t "$pkgdir/usr/bin"
	install -Dm644 ENDROLL.desktop -t "$pkgdir/usr/share/applications"
	mkdir -p "$pkgdir/usr/lib"
	mv 'EndRoll201' "$pkgdir/usr/lib/ENDROLL"
}
