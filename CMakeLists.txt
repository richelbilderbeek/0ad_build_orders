cmake_minimum_required(VERSION 3.5)

project(0ad_build_orders LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_executable(0ad_build_orders
    include/helper.h
    src/helper.cpp
    src/main.cpp
)
