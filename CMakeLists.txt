cmake_minimum_required(VERSION 3.2)
project(playground LANGUAGES Fortran)

add_subdirectory(${CMAKE_SOURCE_DIR}/src stufflib)
add_subdirectory(${CMAKE_SOURCE_DIR}/external/pFUnit)
add_subdirectory(${CMAKE_SOURCE_DIR}/test)