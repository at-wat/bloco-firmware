#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.61)
AC_INIT([bloco-firmware], [1.14.0], [atsushi.w@openspur.org])
AM_INIT_AUTOMAKE

AM_MAINTAINER_MODE([disable])

AC_CONFIG_HEADERS([include/config.h])

# Define Vendor
AC_DEFINE(YP_VENDOR_NAME, "Univ. of Tsukuba - Intelligent Robot Lab.", vendor)
AC_DEFINE(YP_PRODUCT_NAME, "Yamabico Project - Spur", product)
AC_DEFINE(YP_FIRMWARE_NAME, "2013.10.18", firmware)
AC_DEFINE(YP_PROTOCOL_NAME, "YPP:06:00", protocol)

# Checks for SH_CROSS
AC_CHECK_PROGS(SH_CROSS_CC, sh-coff-gcc sh-hitachi-coff-gcc,, $PATH)
AC_CHECK_PROGS(SH_CROSS_AR, sh-coff-ar sh-hitachi-coff-ar,, $PATH)
AC_CHECK_PROGS(SH_CROSS_OBJCOPY, sh-coff-objcopy sh-hitachi-coff-objcopy,, $PATH)
AM_CONDITIONAL(HAVE_SH_CROSS, test -n "$SH_CROSS_CC")

AC_CHECK_PROGS(SH_CROSS_ELF_CC, sh-elf-gcc sh-hitachi-elf-gcc,, $PATH)
AC_CHECK_PROGS(SH_CROSS_ELF_AR, sh-elf-ar sh-hitachi-elf-ar,, $PATH)
AC_CHECK_PROGS(SH_CROSS_ELF_OBJCOPY, sh-elf-objcopy sh-hitachi-elf-objcopy,, $PATH)
AM_CONDITIONAL(HAVE_SH_ELF_CROSS, test -n "$SH_CROSS_ELF_CC")

AC_CONFIG_FILES([
 Makefile
 target-sh/Makefile
])

AC_OUTPUT

