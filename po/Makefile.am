LANGUAGES = de ru
PO_FILES = de.po ru.po

# END CONFIG ##################################################################

.PHONY: all install install-user uninstall uninstall-user clean $(LANGUAGES)
.PHONY: update-po update-pot

all: $(LANGUAGES)

$(LANGUAGES):
	if [[ -e $(srcdir)/$@.po ]]; \
	then $(MSGFMT) -c -v -o $(builddir)/$@.mo $(srcdir)/$@.po; \
	else $(MSGFMT) -c -v -o $(builddir)/$@.mo $(builddir)/$@.po; \
	fi

update-po: $(PO_FILES)

$(PO_FILES): $(GETTEXT_PACKAGE).pot
	if [[ -e $(srcdir)/$@ ]]; \
	then $(MSGMERGE) -U $(srcdir)/$@ $^; \
	else $(MSGFMT) -l $(subst .po,,$@) -o $(builddir)/$@ -i $^; \
	fi

@SNIPPET3@

install-data-local: $(LANGUAGES)
	for L in $(LANGUAGES); \
	do $(MKDIR_P) -p "$(DESTDIR)$(gimplocalesdir)/$$L/LC_MESSAGES"; \
	install -v -m 0644 $(builddir)/$$L.mo "$(DESTDIR)$(gimplocalesdir)/$$L/LC_MESSAGES/$(GETTEXT_PACKAGE).mo"; \
	done

uninstall-local: $(LANGUAGES)
	for L in $(LANGUAGES); \
	do rm -vf "$(DESTDIR)$(gimplocalesdir)/$$L/LC_MESSAGES/$(GETTEXT_PACKAGE).mo"; \
	done

clean-local:
	rm -f *.po~ *.mo *.mo~

install-user:
	$(warning Will not install gettext files for user installation!)

uninstall-user:
	$(warning Will not uninstall gettext files for user installation!)

$(GETTEXT_PACKAGE).pot: $(top_srcdir)/scripts/*.scm $(top_srcdir)/src/*.c
	$(XGETTEXT) -C -k_ -kN_ -d $(GETTEXT_PACKAGE) -o $@ $^

update-pot: $(GETTEXT_PACKAGE).pot

EXTRA_DIST = $(PO_FILES) $(GETTEXT_PACKAGE).pot
