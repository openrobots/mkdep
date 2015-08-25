dnl autoconf script for mkdep
dnl
AC_INIT([mkdep],[2.8],[http://softs.laas.fr/openrobots/], mkdep)
AC_PREREQ(2.59)
AM_INIT_AUTOMAKE([foreign dist-bzip2])

AC_CONFIG_HEADER([config.h])

AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_INSTALL
AC_CHECK_HEADERS(unistd.h, [], AC_MSG_ERROR("Not a POSIX system"))
AC_REPLACE_FUNCS(strlcat strlcpy)
AC_C_CONST

dnl
dnl Get cannonical host
dnl
AC_CANONICAL_HOST
AC_DEFINE_UNQUOTED(OS_TYPE, "$host_os")

AC_SUBST(exeext)
case ${host_os} in
   cygwin*)
   exeext=.exe
   ;;
esac

AC_OUTPUT(Makefile mkdep.pc)
