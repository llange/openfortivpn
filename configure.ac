#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([openfortivpn], [1.6.0])
AC_CONFIG_SRCDIR([src/main.c])
AM_INIT_AUTOMAKE([foreign subdir-objects])

# Checks for programs.
AC_PROG_CC
AC_GNU_SOURCE

# Helps support multiarch by setting 'host_os' and 'host_cpu'
AC_CANONICAL_HOST

AM_SILENT_RULES([yes])

# Checks for libraries.
PKG_CHECK_MODULES(OPENSSL, [libcrypto libssl])
AC_CHECK_LIB([pthread], [pthread_create], [], [AC_MSG_ERROR([Cannot find libpthread.])])
AC_CHECK_LIB([util], [forkpty], [], [AC_MSG_ERROR([Cannot find libutil.])])

# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h fcntl.h netdb.h netinet/in.h stddef.h stdint.h stdlib.h string.h strings.h sys/ioctl.h sys/socket.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_OFF_T
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([getaddrinfo inet_ntoa ntohs memmove memset memmem select socket strerror strstr strtol])

AC_OUTPUT(Makefile)
