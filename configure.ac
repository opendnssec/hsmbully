#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.61)
AC_INIT([hsmbully],[0.0.1],[rick@openfortress.nl])
AM_INIT_AUTOMAKE
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([src/hsmbully.c])
AC_CONFIG_HEADER([config.h])

AC_USE_SYSTEM_EXTENSIONS

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_LIBTOOL

ACX_PEDANTIC
ACX_STRICT
 
# Checks for header files.
AC_HEADER_STDC
AC_HEADER_STDBOOL
AC_CHECK_HEADERS([stdlib.h stdio.h math.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC

ACX_CUNIT
ACX_DLOPEN

AC_ARG_WITH(pkcs11, 
	AC_HELP_STRING([--with-pkcs11=PATH],[specify path of PKCS#11 library to use]),
	[ pkcs11_module="$withval" ],
	[ pkcs11_module="$prefix/lib/libsofthsm.so" ]
)

AC_SUBST(pkcs11_module)

AC_CONFIG_FILES([
Makefile
src/Makefile
])

AC_OUTPUT