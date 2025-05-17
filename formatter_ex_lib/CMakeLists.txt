cmake_minimum_required(VERSION 3.4)
project(formatter_ex)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_SOURCE_DIR}/formatter_lib)  # <- путь к formatter.h

add_library(formatter_ex STATIC formatter_ex.cpp)
target_link_libraries(formatter_ex formatter)
