#------------------------
# test_s4
#------------------------

bin_PROGRAMS += sfifos_test_s4.out

sfifos_test_s4_out_SOURCES = \
   oros/common/src/sfifos/tests/test_s4/main.c

nodist_sfifos_test_s4_out_SOURCES = \
   oros/common/src/sfifos/tests/test_s4/__fifos__.h \
   oros/common/src/sfifos/tests/test_s4/__fifos__.c \
   oros/common/src/sfifos/tests/test_s4/__atoms__.h \
   oros/common/src/sfifos/tests/test_s4/__atoms__.c

sfifos_test_s4_out_CLEANFILES = \
   oros/common/src/sfifos/tests/test_s4/__fifos__.h \
   oros/common/src/sfifos/tests/test_s4/__fifos__.c \
   oros/common/src/sfifos/tests/test_s4/__atoms__.h \
   oros/common/src/sfifos/tests/test_s4/__atoms__.c

EXTRA_DIST += \
   oros/common/src/sfifos/tests/test_s4/fifos.or \
   oros/common/src/sfifos/tests/test_s4/atoms.or

BUILT_SOURCES += af_s4

af_s4:
	_create_af$(EXEEXT) \
		$(top_srcdir)/oros/common/src/sfifos/tests/test_s4/fifos.or \
		$(top_srcdir)/oros/common/src/sfifos/tests/test_s4/atoms.or \
		oros/common/src/sfifos/tests/test_s4/__fifos__.h \
		oros/common/src/sfifos/tests/test_s4/__fifos__.c \
		oros/common/src/sfifos/tests/test_s4/__atoms__.h \
		oros/common/src/sfifos/tests/test_s4/__atoms__.c 

sfifos_test_s4_out_LDADD = \
   osl/lib.osl.a \
   oros/common/src/sfifos/lib/edmadriver/lib.oros.common.sfifos.edmadriver.a \
   oros/common/src/sfifos/lib/ipc/lib.oros.common.sfifos.ipc.a \
   oros/common/src/sfifos/lib.oros.common.sfifos.a \
   lib.oros.common.sfifos.test_blocks.a

sfifos_test_s4_out_CFLAGS = -I"$(top_srcdir)/oros/common/src/sfifos/tests/test_blocks"
sfifos_test_s4_out_CFLAGS += -Ioros/common/src/sfifos/tests/test_s4

sfifos_test_s4_out_LDFLAGS=\
--LINKER_SCRIPT_FILE "`_cygpath -w \"$(top_srcdir)/memorymaps/$(MEMORYMAP_FILE)\"`"
