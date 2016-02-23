SUBDIRS = btc_channel_electrum

bin_SCRIPTS = btc-channel-electrum
CLEANFILES = $(bin_SCRIPTS)
EXTRA_DIST = btc-channel-electrum.in

do_substitution = sed -e 's,[@]pythondir[@],$(pythondir),g' \
	-e 's,[@]PACKAGE[@],$(PACKAGE),g' \
	-e 's,[@]VERSION[@],$(VERSION),g' 

btc-channel-electrum: btc-channel-electrum.in Makefile
	$(do_substitution) < $(srcdir)/btc-channel-electrum.in > btc-channel-electrum
	chmod +x btc-channel-electrum

install-data-local:
	mkdir -p /var/lib/btc-channel-electrum