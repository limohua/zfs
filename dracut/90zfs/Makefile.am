pkgdracutdir = $(datadir)/dracut/modules.d/90zfs
dist_pkgdracut_SCRIPTS = \
	$(top_srcdir)/dracut/90zfs/90-zfs.rules \
	$(top_srcdir)/dracut/90zfs/check \
	$(top_srcdir)/dracut/90zfs/install \
	$(top_srcdir)/dracut/90zfs/installkernel \
	$(top_srcdir)/dracut/90zfs/mount-zfs.sh \
	$(top_srcdir)/dracut/90zfs/zfs-genrules.sh \
	$(top_srcdir)/dracut/90zfs/parse-zfs.sh

all:
	@list='$(dist_pkgdracut_SCRIPTS)'; \
	for file in $$list; do \
		link=$$(basename $$file); \
		if [ ! -e $$link ]; then \
			$(LN_S) $$file $$link; \
		fi \
	done

clean:
	@list='$(dist_pkgdracut_SCRIPTS)'; \
	for file in $$list; do \
		link=$$(basename $$file); \
		if [ -L $$link ]; then \
			$(RM) $$link; \
		fi \
	done
