project(stufflib LANGUAGES Fortran)

set(CMAKE_Fortran_FLAGS "-cpp -fPIC -fdefault-real-8 -fdefault-double-8 -frecursive -Wno-unused-function -Wno-unused-variable")
add_library(stuff ${CMAKE_CURRENT_SOURCE_DIR}/stuff.f90)