cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  SetFileAttributesW.c
)

add_executable(paltest_setfileattributesw_test3
  ${SOURCES}
)

add_dependencies(paltest_setfileattributesw_test3 CoreClrPal)

target_link_libraries(paltest_setfileattributesw_test3
  pthread
  rt
  m
  CoreClrPal
)
