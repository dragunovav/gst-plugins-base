plugin_LTLIBRARIES = libgstplayback.la

csp_cflags = -DCOLORSPACE=\"videoconvert\"

libgstplayback_la_SOURCES = \
	gstdecodebin2.c \
	gsturidecodebin.c \
	gstplayback.c \
	gstplaybin2.c \
	gstplaysink.c \
	gstplay-enum.c \
	gstsubtitleoverlay.c \
	gstplaysinkvideoconvert.c \
	gstplaysinkaudioconvert.c \
	gstplaysinkconvertbin.c \
	gststreamsynchronizer.c \
	gstplaybackutils.c

nodist_libgstplayback_la_SOURCES = $(built_sources)
libgstplayback_la_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS) $(csp_cflags)
libgstplayback_la_LDFLAGS = $(GST_PLUGIN_LDFLAGS)
libgstplayback_la_LIBADD = \
	$(top_builddir)/gst-libs/gst/pbutils/libgstpbutils-@GST_API_VERSION@.la \
	$(top_builddir)/gst-libs/gst/audio/libgstaudio-@GST_API_VERSION@.la \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-@GST_API_VERSION@.la \
	$(GST_LIBS)
libgstplayback_la_LIBTOOLFLAGS = $(GST_PLUGIN_LIBTOOLFLAGS)

noinst_HEADERS = \
	gstplayback.h \
	gstplaysink.h \
	gstplay-enum.h \
	gstrawcaps.h \
	gstsubtitleoverlay.h \
	gstplaysinkvideoconvert.h \
	gstplaysinkaudioconvert.h \
	gstplaysinkconvertbin.h \
	gststreamsynchronizer.h \
	gstplaybackutils.h

BUILT_SOURCES = $(built_headers) $(built_sources)

CLEANFILES = $(BUILT_SOURCES)
