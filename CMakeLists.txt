#
# project: fips-lua
#
cmake_minimum_required(VERSION 2.8)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

fips_setup()
fips_project(fips-lua)

fips_begin_lib(lua)
fips_src(lua/ NO_RECURSE)
fips_end_lib()

fips_finish()


