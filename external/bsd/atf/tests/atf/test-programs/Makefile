# $NetBSD: Makefile,v 1.2 2010/07/13 21:12:39 jmmv Exp $

.include <bsd.own.mk>

TESTSDIR=	${TESTSBASE}/atf/test-programs
ATFFILE=	yes

SRCDIR=		${NETBSDSRCDIR}/external/bsd/atf/dist
.PATH:		${SRCDIR}/test-programs

CPPFLAGS+=	-DHAVE_CONFIG_H
CPPFLAGS+=	-I${SRCDIR}/libs -I${SRCDIR}

TESTS_C=	c_helpers

TESTS_CXX=	cpp_helpers

TESTS_SH=	sh_helpers
.for t in config_test expect_test fork_test meta_data_test result_test \
          srcdir_test
TESTS_SH+=		${t}
TESTS_SH_SRC_${t}=	common.sh ${t}.sh
.endfor

.include <bsd.test.mk>
