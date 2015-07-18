NO_WERROR = 1

SUBDIR=logger.tproj


INSTALLDIRS= ${DESTDIR}/usr/bin ${DESTDIR}/usr/share/man/man1 
# If we could change gid before running mkdir we could remove these
INSTALLDIRS += ${DESTDIR}/usr/share ${DESTDIR}/usr/share/man

installsrc: clean
	cp -rp . ${SRCROOT}

installhdrs:
	true

beforeinstall:
	-mkdir -p ${INSTALLDIRS}
	-chgrp wheel ${INSTALLDIRS}

afterinstall:
	# COMPRESSMANPAGES use DSTROOT automatically
	/Developer/Makefiles/bin/compress-man-pages.pl -d ${DESTDIR} /usr/share/man

.include <bsd.subdir.mk>
