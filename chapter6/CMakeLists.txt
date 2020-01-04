cmake_minimum_required(VERSION 3.13)
project(ch6_main)

set(CMAKE_CXX_STANDARD 11)

add_executable(ch6_main chap6/ch6_main.cpp)
add_executable(ch6_btree binarytree/btree.cpp)
add_executable(ch6_s_main strategy/s_main.cpp)