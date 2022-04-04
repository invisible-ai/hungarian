cmake_minimum_required(VERSION 3.0.0)
project("Hungarian Algorithm")

set(CMAKE_CXX_STANDARD 11)

add_library(hungarian SHARED hungarian.cpp)
target_include_directories(hungarian PUBLIC .)

add_executable(test_cases test.cpp)
target_link_libraries(test_cases hungarian)

install(TARGETS hungarian
        LIBRARY DESTINATION $ENV{HOME}/.local/lib)
