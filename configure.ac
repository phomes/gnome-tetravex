AC_PREREQ([2.63])
AC_INIT([GNOME Tetravex], [3.22.0], [https://bugzilla.gnome.org/],
        [gnome-tetravex], [https://wiki.gnome.org/Apps/Tetravex])
AC_CONFIG_MACRO_DIR([m4])

AM_INIT_AUTOMAKE([1.11 no-dist-gzip dist-xz foreign])
AM_SILENT_RULES([yes])
AM_MAINTAINER_MODE

AM_PROG_VALAC([0.24])
AM_PROG_CC_C_O

GLIB_GSETTINGS

APPSTREAM_XML

dnl ###########################################################################
dnl Dependencies
dnl ###########################################################################

GLIB_REQUIRED=2.40.0
GTK_REQUIRED=3.13.4

PKG_CHECK_MODULES(GNOME_TETRAVEX, [
  gio-2.0 >= $GLIB_REQUIRED
  glib-2.0 >= $GLIB_REQUIRED
  gtk+-3.0 >= $GTK_REQUIRED
])

AC_SUBST([GLIB_REQUIRED])

AC_PATH_PROG([DESKTOP_FILE_VALIDATE], [desktop-file-validate], [/bin/true])

dnl ###########################################################################
dnl GResources
dnl ###########################################################################

AC_PATH_PROG(GLIB_COMPILE_RESOURCES,glib-compile-resources)

dnl ###########################################################################
dnl Internationalization
dnl ###########################################################################

IT_PROG_INTLTOOL([0.50])
AC_SUBST(GETTEXT_PACKAGE, gnome-tetravex)

dnl ###########################################################################
dnl Documentation
dnl ###########################################################################

YELP_HELP_INIT

dnl ###########################################################################
dnl Files to generate
dnl ###########################################################################

AC_CONFIG_FILES([
Makefile
po/Makefile.in
data/Makefile
data/icons/Makefile
data/icons/hicolor/Makefile
help/Makefile
src/Makefile
])
AC_OUTPUT
