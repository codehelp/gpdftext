
gladedir = $(datadir)/gpdftext/glade
glade_DATA = gpdftext.glade

AM_CPPFLAGS = \
	$(GPDFTEXT_CFLAGS)

AM_CFLAGS =\
	$(WARN_CFLAGS) \
	 -Wall\
	 -g

bin_PROGRAMS = gpdftext

gpdftext_SOURCES = \
	ebookui.c \
	ebookui.h \
	main.c \
	pdf.c \
	pdf.h \
	spell.c \
	spell.h

gpdftext_LDFLAGS = \
	-Wl,--export-dynamic -Wl,-z,defs -Wl,--as-needed

gpdftext_LDADD = $(GPDFTEXT_LIBS)

EXTRA_DIST = $(glade_DATA)

# Remove glade directory on uninstall
uninstall-local:
	-rm -r $(gladedir)
	-rm -r $(datadir)/gpdftext
