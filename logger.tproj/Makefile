THIS=$(shell basename `pwd` .tproj)

install:: all

all installhdrs installsrc clean ${THIS} install::
	env MAKEOBJDIR=${OBJROOT} bsdmake ARCH_FLAGS="${RC_CFLAGS}" NO_MANCOMPRESS=true DESTDIR=${DSTROOT} -f BSDmakefile $@
