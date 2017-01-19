cmake_minimum_required(VERSION 3.5)

project(spline)


# this is a hack. Find a better way to include spline project dependency.
#include_directories(SYSTEM ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_library(spline STATIC src/spline.h)
set_target_properties(spline PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(spline PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

