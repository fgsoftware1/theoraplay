cmake_minimum_required(VERSION 3.15)
project(theoraplay LANGUAGES C)

find_package(unofficial-theora CONFIG REQUIRED)
find_package(Vorbis CONFIG REQUIRED)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_library(theoraplay STATIC
    theoraplay.c
)
target_link_libraries(theoraplay PRIVATE unofficial::theora::theora Vorbis::vorbis)