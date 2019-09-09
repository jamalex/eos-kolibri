AC_PREREQ([2.63])
AC_INIT([eos-kolibri], [1.0.0], [dylan@endlessm.com])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE([1.11 -Wno-portability foreign no-define tar-ustar no-dist-gzip dist-xz])
AM_MAINTAINER_MODE([enable])
AM_SILENT_RULES([yes])

PKG_PROG_PKG_CONFIG

# For systemd
PKG_CHECK_EXISTS([systemd], [],
	[AC_MSG_ERROR([systemd required to build $PACKAGE_NAME])])

AC_ARG_WITH([systemdsystemunitdir],
	[AS_HELP_STRING([--with-systemdsystemunitdir],
			[systemd unit file directory])],
	[systemdsystemunitdir=$withval],
	[systemdsystemunitdir=`$PKG_CONFIG --variable=systemdsystemunitdir systemd`])
AS_IF([test "x$systemdsystemunitdir" = x],
	[AC_MSG_ERROR([no path for systemd unit directory])])
AC_SUBST([systemdsystemunitdir])

AC_ARG_VAR(KOLIBRI_PORT, port number for system Kolibri instance (default: 18009))

if test -z "$KOLIBRI_PORT"; then
	KOLIBRI_PORT=18009
fi

AC_CONFIG_FILES([
Makefile
data/Makefile
])
AC_OUTPUT

echo "
    eos-kolibri $VERSION
"
