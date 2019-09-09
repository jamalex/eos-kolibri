%: %.in Makefile
	$(AM_V_GEN) sed -e "s|\@bindir\@|$(bindir)|" -e "s|\@KOLIBRI_PORT\@|$(KOLIBRI_PORT)|" $<> $@

# systemd files for socket activated service
systemdsystemunit_DATA = \
	eos-kolibri-system-helper.service \
	eos-kolibri-system-helper.socket \
	$(NULL)

# systemd tmpfiles.d
tmpfilesdir = $(prefix)/lib/tmpfiles.d
tmpfiles_DATA = eos-kolibri-system-helper.conf

# flatpak overrides
flatpakoverridesdir = $(localstatedir)/lib/flatpak/overrides
flatpakoverrides_DATA = org.learningequality.Kolibri

EXTRA_DIST = \
	eos-kolibri-system-helper.service \
	eos-kolibri-system-helper.socket \
	eos-kolibri-system-helper.conf \
	$(NULL)

CLEANFILES = \
	eos-kolibri-system-helper.service \
	eos-kolibri-system-helper.socket \
	$(NULL)
