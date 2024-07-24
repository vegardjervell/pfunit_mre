#Example project using `pFUnit` with `add_submodule`

To build and run tests, execute the shell script `build_and_run_tests.sh`.

This project was made in order to figure out how to get `pFUnit` to properly build as a git submodule. I was experiencing quite a few issues that were arising from how I was setting compiler flags for my library and test suite, and that the compiler flags I was using did not play nicely with `add_subdirectory(pFUnit)`. 

The working solution I ended up with is the one found here, where the top-level `CMakeLists.txt` does nothing more than `add_subdirectory` to include the main library, the test suite and `pFUnit` as subprojects.

This build system has been tested to work using
  * MacOS 12.5.1
  * gfortran 13.2.0 (Homebrew)
  * gcc 13.2.0 (Homebrew)
  * g++ 13.2.0 (Homebrew)
  * cmake 3.24.2
  * make 3.81
  * pFUnit 4.10
