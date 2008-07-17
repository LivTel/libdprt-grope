# $Header: /space/home/eng/cjm/cvs/libdprt-grope/test/Makefile,v 1.2 2008-07-17 10:50:56 cjm Exp $

include	../../../Makefile.common
include ../../Makefile.common
include ../Makefile.common

LIBNAME		= $(LIBDPRT_HOME)_$(GROPE_HOME)
INCDIR 		= $(LIBDPRT_GROPE_SRC_HOME)/include
DOCSDIR 	= $(LIBDPRT_GROPE_DOC_HOME)/test
DOCFLAGS 	= -static
BINDIR		= $(LIBDPRT_GROPE_BIN_HOME)/test/${HOSTTYPE}

CFLAGS 		= -g -I$(INCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR) -I$(JNIGENERALINCDIR) 

SRCS 		= dprt_test.c
OBJS 		= $(SRCS:%.c=$(BINDIR)/%.o)
DOCS 		= $(SRCS:%.c=$(DOCSDIR)/%.html)

top: ${BINDIR}/dprt_test docs

${BINDIR}/dprt_test: $(BINDIR)/dprt_test.o $(LT_LIB_HOME)/$(LIBNAME).so
	$(CC) -o $@ $(BINDIR)/dprt_test.o -L$(LT_LIB_HOME) -ldprt_grope -ldprt_jni_general $(TIMELIB) -lm -lc

$(BINDIR)/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

docs: $(DOCS)

$(DOCS) : $(SRCS)
	-$(CDOC) -d $(DOCSDIR) -h $(INCDIR) $(DOCFLAGS) $(SRCS)

depend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS) -- $(SRCS)

clean:
	-$(RM) $(RM_OPTIONS) ${BINDIR}/dprt_test $(OBJS) $(TIDY_OPTIONS)

tidy:
	-$(RM) $(RM_OPTIONS) $(TIDY_OPTIONS)

backup: tidy
	-$(RM) $(RM_OPTIONS) $(LIBDPRT_BIN_HOME)/test/dprt_test

checkin:
	-$(CI) $(CI_OPTIONS) $(SRCS)

checkout:
	$(CO) $(CO_OPTIONS) $(SRCS)

#
# $Log: not supported by cvs2svn $
# Revision 1.1  2005/11/29 16:01:43  cjm
# Initial revision
#
# Revision 1.1  2005/03/11 11:56:57  cjm
# Initial revision
#
#

# DO NOT DELETE

/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/stdio.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/features.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/sys/cdefs.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/gnu/stubs.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stddef.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/types.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/wordsize.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/typesizes.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/libio.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/_G_config.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/wchar.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/wchar.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/gconv.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stdarg.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/stdio_lim.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/bits/sys_errlist.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/stdlib.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/include/strings.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /home/dev/src/libdprt/grope/include/dprt.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/java/j2sdk1.4.2_06/include/jni.h
/home/dev/bin/libdprt/grope/test/i386-linux/dprt_test.o: /usr/java/j2sdk1.4.2_06/include/linux/jni_md.h
