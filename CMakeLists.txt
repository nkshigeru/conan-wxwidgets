cmake_minimum_required(VERSION 2.8.12)
project(cmake_wrapper)

include(conanbuildinfo.cmake)
conan_basic_setup()

# find standard libraries before frameworks. avoid finding wrong library in Mono.framework
set(CMAKE_FIND_FRAMEWORK LAST)

add_subdirectory("source_subfolder")
