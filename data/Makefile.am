# systemd files for socket activated service
systemdsystemunit_DATA = \
	eos-kolibri-system-helper.service \
	eos-kolibri-system-helper.socket \
	$(NULL)

%.service: %.service.in Makefile
	$(AM_V_GEN) sed -e "s|\@bindir\@|$(bindir)|" $<> $@

# systemd tmpfiles.d
tmpfilesdir = $(prefix)/lib/tmpfiles.d
tmpfiles_DATA = eos-kolibri-system-helper.conf

EXTRA_DIST = \
	eos-kolibri-system-helper.service.in \
	eos-kolibri-system-helper.socket \
	$(tmpfiles_DATA) \
	$(NULL)

CLEANFILES = \
	eos-kolibri-system-helper.service \
	$(NULL)
