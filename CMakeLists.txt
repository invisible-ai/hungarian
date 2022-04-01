cmake_minimum_required(VERSION 3.0.0)
project("Hungarian Algorithm")

set(CMAKE_CXX_STANDARD 11)

add_library(hungarian hungarian.cpp hungarian.hpp)
target_compile_options(hungarian PRIVATE -fPIC)

add_executable(test_cases test.cpp)
target_link_libraries(test_cases hungarian)
