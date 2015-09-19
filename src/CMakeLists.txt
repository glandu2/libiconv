cmake_minimum_required(VERSION 2.8)

file(GLOB_RECURSE SOURCE_FILES *.c *.h ${ICONV_INCLUDE}/*.h)

if(BUILD_SHARED_LIBS)
  add_definitions(-DBUILDING_LIBICONV)
endif()

add_library(${TARGET_NAME} ${SOURCE_FILES})

