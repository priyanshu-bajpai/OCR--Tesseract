SUBDIRS =
AM_CPPFLAGS = -I$(top_srcdir)/ccutil -I$(top_srcdir)/viewer

include_HEADERS = \
    bitvec.h callcpp.h const.h cutil.h cutil_class.h danerror.h efio.h \
    emalloc.h freelist.h globals.h listio.h \
    oldheap.h oldlist.h structures.h tessarray.h

if !USING_MULTIPLELIBS
noinst_LTLIBRARIES = libtesseract_cutil.la
else
lib_LTLIBRARIES = libtesseract_cutil.la
libtesseract_cutil_la_LDFLAGS = -version-info $(GENERIC_LIBRARY_VERSION)
libtesseract_cutil_la_LIBADD = \
	../ccutil/libtesseract_ccutil.la \
	../viewer/libtesseract_viewer.la	
endif

libtesseract_cutil_la_SOURCES = \
    bitvec.cpp callcpp.cpp cutil.cpp cutil_class.cpp danerror.cpp efio.cpp \
    emalloc.cpp freelist.cpp listio.cpp oldheap.cpp \
    oldlist.cpp structures.cpp tessarray.cpp


