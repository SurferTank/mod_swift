CLEANFILES = libmod_swift.so libmod_swift_old.so *~

lib_LTLIBRARIES = mod_swift.la
mod_swift_la_SOURCES = mod_swift.c mod_swift.h
mod_swift_la_LDFLAGS = -module
mod_swift_la_DEPENDENCIES = ../include/config.h
#/usr/sbin/apxs -c -I../include -I. -D HAVE_CONFIG_H mod_mono.c
mod_swift_la_CFLAGS = -Wall -DDFLT_SWIFT_CONFIG_DIR=\"$(DFLT_SWIFT_CONFIG_DIR)\"

install: $(lib_LTLIBRARIES)
    $(mkinstalldirs) "$(DESTDIR)$(APXS_LIBEXECDIR)"
    $(APXS) -S LIBEXECDIR="$(DESTDIR)$(APXS_LIBEXECDIR)" -i -n swift mod_swift.la