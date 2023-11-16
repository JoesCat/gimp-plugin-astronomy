## Process this file with automake to produce Makefile.in

SUBDIRS = . scripts src doc po

ACLOCAL_AMFLAGS = -I m4

EXTRA_DIST = \
	ABOUT-NLS \
	autogen.sh \
	rpm/gimp-plugin-astronomy.spec.in

nodist_EXTRA_DATA = .git .github

AUTOMAKE_OPTIONS = foreign dist-bzip2

strip:
	$(STRIP) ${builddir}/src/astronomy-alignment
	$(STRIP) ${builddir}/src/astronomy-artificial-galaxy
	$(STRIP) ${builddir}/src/astronomy-artificial-stars
	$(STRIP) ${builddir}/src/astronomy-background-gradient
	$(STRIP) ${builddir}/src/astronomy-merge
	$(STRIP) ${builddir}/src/astronomy-star-rounding
