AC_PREREQ(2.60)

AC_INIT(c-capnproto, 0.1, [])
AC_CONFIG_SRCDIR(lib/capnp_c.h)
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_AUX_DIR([ac])

AC_CANONICAL_BUILD()
AC_CANONICAL_HOST()
AC_CANONICAL_TARGET()

AM_INIT_AUTOMAKE(1.11)
AM_SILENT_RULES([yes])
AC_CONFIG_HEADERS([config.h])

AC_USE_SYSTEM_EXTENSIONS

LT_INIT

AC_LANG([C])
AC_PROG_CC
AC_PROG_CXX

AC_PROG_INSTALL
AC_PROG_LN_S

AC_ARG_ENABLE(werror,
  AS_HELP_STRING([--enable-werror], [enable -Werror (for developers only)]))
if test x"${enable_werror}" = x"yes" ; then
  WERROR="-Werror"
fi
AC_SUBST(WERROR)

#PKG_CHECK_MODULES(CAPNP, [capnp >= 0.5.2], [], [
#  AC_MSG_ERROR([capnproto base package (0.5.2 or newer) not found])
#])

AC_CONFIG_SUBDIRS([gtest/googletest])

AC_CONFIG_FILES([
	Makefile
	c-capnproto.pc
])
AC_OUTPUT
