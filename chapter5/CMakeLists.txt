cmake_minimum_required(VERSION 3.13)
project(ch5_main)

set(CMAKE_CXX_STANDARD 11)

add_executable(ch5_main chap5/c5_main.cpp)
add_executable(ch5_hybrid hybrid/hybrid.cpp)
add_executable(ch5_inher inher/classes.cpp)