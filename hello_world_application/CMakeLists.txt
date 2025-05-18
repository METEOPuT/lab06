cmake_minimum_required(VERSION 3.4)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world hello_world.cpp)

if (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    target_link_libraries(hello_world PRIVATE stdc++)
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "Clang")
    target_link_libraries(hello_world PRIVATE c++)
endif()

target_link_libraries(hello_world PRIVATE formatter_ex_lib)
