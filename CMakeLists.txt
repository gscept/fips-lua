#
# project: fips-lua
#
cmake_minimum_required(VERSION 3.21)

if (NOT FIPS_IMPORT)
# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    project(fips-lua)
    fips_setup()
endif()


fips_begin_lib(lua)
fips_src(lua/ NO_RECURSE)
fips_end_lib()

