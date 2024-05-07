cmake_minimum_required (VERSION 3.9)
project (geometry)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_compile_options(-g -Wall -Wextra -Wpedantic -Wl,--stack,16777216)

add_executable(raytracer raytracer.cc math_test.cc math.h math.tcc math.cc geometry.cc geometry.h geometry.tcc geometry_test.cc
        geometry.h
        math.h
        color.h)
target_link_libraries(raytracer gtest gtest_main)