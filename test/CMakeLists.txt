cmake_policy(SET CMP0074 NEW)

set(CMAKE_Fortran_FLAGS "-cpp -fPIC -fdefault-real-8 -fdefault-double-8 -frecursive -Wno-unused-function -Wno-unused-variable")

# add_subdirectory(${CMAKE_SOURCE_DIR}/external/pFUnit pFUnit)
enable_testing()
file(GLOB UNITTEST_SRC ${CMAKE_CURRENT_SOURCE_DIR}/*.pf)
add_pfunit_ctest(mytests TEST_SOURCES ${UNITTEST_SRC} LINK_LIBRARIES stuff)
target_include_directories(mytests PRIVATE ${CMAKE_BINARY_DIR}/stufflib ${CMAKE_CURRENT_BINARY_DIR})