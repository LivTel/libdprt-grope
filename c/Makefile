# $Header: /space/home/eng/cjm/cvs/libdprt-grope/c/Makefile,v 1.2 2008-07-17 10:50:32 cjm Exp $

include	../../../Makefile.common
include	../../Makefile.common
include	../Makefile.common

LIBNAME		= $(LIBDPRT_HOME)_$(GROPE_HOME)
INCDIR 		= $(LIBDPRT_GROPE_SRC_HOME)/include
DOCSDIR 	= $(LIBDPRT_GROPE_DOC_HOME)/cdocs
BINDIR		= $(LIBDPRT_GROPE_BIN_HOME)/c/$(HOSTTYPE)
CFLAGS 		= -g $(CCHECKFLAG) -I$(INCDIR) -I$(CFITSIOINCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR) \
		-I$(JNIGENERALINCDIR) -L$(LT_LIB_HOME)
LINTFLAGS 	= -I$(INCDIR) -I$(JNIINCDIR) -I$(JNIMDINCDIR)
DOCFLAGS 	= -static
SRCS 		= dprt.c ngat_dprt_grope_DpRtLibrary.c
HEADERS		= $(SRCS:%.c=%.h)
OBJS		= $(SRCS:%.c=$(BINDIR)/%.o)
DOCS 		= $(SRCS:%.c=$(DOCSDIR)/%.html)
LIBS		= -lcfitsio -ldprt_jni_general

top: shared docs

shared: $(INCDIR)/ngat_dprt_grope_DpRtLibrary.h $(LT_LIB_HOME)/$(LIBNAME).so

$(INCDIR)/ngat_dprt_grope_DpRtLibrary.h: $(DPRT_BIN_HOME)/java/ngat/dprt/grope/DpRtLibrary.class
	$(JAVAH) -jni -d $(INCDIR) -classpath $(DPRT_BIN_HOME)/java:$(CLASSPATH) ngat.dprt.grope.DpRtLibrary
	$(TOUCH) $@

$(LT_LIB_HOME)/$(LIBNAME).so: $(OBJS)
	$(CC) $(CCSHAREDFLAG) $(CFLAGS) $(OBJS) -o $@ $(TIMELIB) $(LIBS) $(SOCKETLIB)

$(BINDIR)/%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

static: $(LT_LIB_HOME)/$(LIBNAME).a

$(LT_LIB_HOME)/$(LIBNAME).a: $(OBJS)
	ar rcv $@ $?

docs: $(DOCS)

$(DOCS) : $(SRCS)
	-$(CDOC) -d $(DOCSDIR) -h $(INCDIR) $(DOCFLAGS) $(SRCS)

# dont checkout ngat_dprt_grope_DpRtLibrary.h - it is a machine built header
checkout:
	$(CO) $(CO_OPTIONS) $(SRCS)
	cd $(INCDIR); $(CO) $(CO_OPTIONS) dprt.h;

# dont checkin ngat_dprt_grope_DpRtLibrary.h - it is a machine built header
checkin:
	-$(CI) $(CI_OPTIONS) $(SRCS)
	-(cd $(INCDIR); $(CI) $(CI_OPTIONS) dprt.h;)

staticdepend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS)  -- $(SRCS)

depend:
	makedepend $(MAKEDEPENDFLAGS) -p$(BINDIR)/ -- $(CFLAGS)  -- $(SRCS)

lint:
	$(LINT)	$(LINTFLAGS) $(SRCS)

clean:
	-$(RM) $(RM_OPTIONS) $(OBJS) $(LT_LIB_HOME)/$(LIBNAME).so $(LT_LIB_HOME)/$(LIBNAME).a 
	-$(RM) $(RM_OPTIONS) $(INCDIR)/ngat_dprt_grope_DpRtLibrary.h $(TIDY_OPTIONS)

tidy:
	-$(RM)  $(RM_OPTIONS) $(TIDY_OPTIONS)
	-cd $(INCDIR); $(RM) $(RM_OPTIONS) $(TIDY_OPTIONS);

backup: tidy
	-$(RM) $(RM_OPTIONS) $(OBJS)

#
# $Log: not supported by cvs2svn $
# Revision 1.1  2007/02/22 18:58:30  cjm
# Initial revision
#
#

# DO NOT DELETE

/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/stdio.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/features.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/sys/cdefs.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/gnu/stubs.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stddef.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/types.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/wordsize.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/typesizes.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/libio.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/_G_config.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/wchar.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/wchar.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/gconv.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stdarg.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/stdio_lim.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/sys_errlist.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/stdlib.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/string.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/math.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/huge_val.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/mathdef.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/bits/mathcalls.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /home/dev/src/cfitsio3.006/include/fitsio.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/include/limits.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/limits.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /home/dev/src/cfitsio3.006/include/longnam.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/java/j2sdk1.4.2_06/include/jni.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /usr/java/j2sdk1.4.2_06/include/linux/jni_md.h
/home/dev/bin/libdprt/grope/c/i386-linux/dprt.o: /home/dev/src/libdprt/grope/include/dprt.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/stdio.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/features.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/sys/cdefs.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/gnu/stubs.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stddef.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/types.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/wordsize.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/typesizes.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/libio.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/_G_config.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/wchar.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/wchar.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/gconv.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/lib/gcc-lib/i386-redhat-linux/3.2.2/include/stdarg.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/stdio_lim.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/bits/sys_errlist.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/stdlib.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/include/string.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/java/j2sdk1.4.2_06/include/jni.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /usr/java/j2sdk1.4.2_06/include/linux/jni_md.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /home/dev/src/libdprt/grope/include/dprt.h
/home/dev/bin/libdprt/grope/c/i386-linux/ngat_dprt_grope_DpRtLibrary.o: /home/dev/src/libdprt/jni_general/include/dprt_jni_general.h
