## Process this file with automake to produce Makefile.in

scm_SCRIPTS = \
	background_gradient_batch.scm \
	border_information.scm \
	brightness_contrast_batch.scm \
	dark_subtraction.scm \
	flat_division.scm \
	mode_batch.scm \
	normalize_batch.scm
scmdir =
# 'make distcheck' can't write to ${GIMP_DATADIR}/scripts/ because of
# directory permissions, therefore don't install programs unless you are root
@SNIPPET2@

EXTRA_DIST = $(scm_SCRIPTS)
