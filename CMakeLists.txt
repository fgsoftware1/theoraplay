cmake_minimum_required(VERSION 3.15)
project(theoraplay LANGUAGES C)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_library(theoraplay STATIC
    theoraplay.c
)