CMAKE_MINIMUM_REQUIRED(VERSION 2.8.7 FATAL_ERROR)

set(CMAKE_VERBOSE_MAKEFILE ON)

# package information
SET(PACKAGE_NAME      "libngx")
SET(PACKAGE_VERSION   "0.1.0")
SET(PACKAGE_STRING    "${PACKAGE_NAME} ${PACKAGE_VERSION}")
SET(PACKAGE_TARNAME   "${PACKAGE_NAME}-${PACKAGE_VERSION}")
SET(PACKAGE_BUGREPORT "https://github.com/mklong/libngx/issues")

PROJECT(${PACKAGE_NAME} C CXX )

set(CFLAGS -pipe  -O -W -Wall -Wpointer-arith -Wno-unused-parameter -Werror -g -O0)

string(REPLACE ";" " " CMAKE_C_FLAGS "${CFLAGS}")
MESSAGE( STATUS ${CMAKE_C_FLAGS} )

#ADD_SUBDIRECTORY(tests)
ADD_SUBDIRECTORY(src)
