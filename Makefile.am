## Process this file with automake to produce Makefile.in

SUBDIRS = . scripts src doc po

EXTRA_DIST = \
	ABOUT-NLS \
	autogen.sh \
	Makefile.mingw \
	config.h.win32 \
	config.rpath \
	m4/codeset.m4 \
	m4/gettext.m4 \
	m4/glibc21.m4 \
	m4/host-cpu-c-abi.m4 \
	m4/iconv.m4 \
	m4/intlmacosx.m4 \
	m4/lcmessage.m4 \
	m4/lib-ld.m4 \
	m4/lib-link.m4 \
	m4/lib-prefix.m4 \
	m4/nls.m4 \
	m4/po.m4 \
	m4/progtest.m4 \
	m4/host-cpu-c-abi.m4 \
	po/de.po \
	po/ru.po \
	po/de.gmo \
	po/ru.gmo \
	po/boldquot.sed \
	po/en@boldquot.header \
	po/en@quot.header \
	po/gimp-plugin-astronomy.pot \
	po/insert-header.sin \
	po/LINGUAS \
	po/Makefile.in \
	po/Makefile.in.in \
	po/Makevars \
	po/Makevars.template \
	po/POTFILES \
	po/POTFILES.in \
	po/quot.sed \
	po/remove-potcdate.sed \
	po/remove-potcdate.sin \
	po/Rules-quot \
	rpm/gimp-plugin-astronomy.spec.in \
	rpm/gimp-plugin-astronomy.spec

nodist_EXTRA_DATA = .git .github

AUTOMAKE_OPTIONS = foreign dist-bzip2

strip:
	$(STRIP) ${builddir}/src/astronomy-alignment
	$(STRIP) ${builddir}/src/astronomy-artificial-galaxy
	$(STRIP) ${builddir}/src/astronomy-artificial-stars
	$(STRIP) ${builddir}/src/astronomy-background-gradient
	$(STRIP) ${builddir}/src/astronomy-merge
	$(STRIP) ${builddir}/src/astronomy-star-rounding
