cmake_minimum_required(VERSION 3.5)

project(0ad_build_orders LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(0ad_build_orders src/main.cpp)
