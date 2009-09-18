# $Id: Makefile.am 1019 2009-06-16 13:16:53Z jakob $

MAINTAINERCLEANFILES = $(srcdir)/Makefile.in

AM_CPPFLAGS =	-I$(srcdir)/.. \
		-I$(srcdir)/cryptoki \
		@CUNIT_INCLUDES@
AM_CFLAGS =	-std=c99

bin_PROGRAMS = hsmbully

hsmbully_LDADD = @CUNIT_LIBS@ -lm

man_MANS = hsmbully.1

EXTRA_DIST =	$(srcdir)/cryptoki/*.h \
		$(srcdir)/hsmbully.1
