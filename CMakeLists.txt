cmake_minimum_required(VERSION 2.6)
project(iconv)

set(TARGET_NAME iconv)

set(ICONV_INCLUDE "${CMAKE_CURRENT_LIST_DIR}/include" CACHE STRING "libiconv include directory")
include_directories(${ICONV_INCLUDE})

add_definitions(-DLIBDIR=\".\" -DICONV_CONST=const -DHAVE_WORKING_O_NOFOLLOW=1)
add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/src" src)
