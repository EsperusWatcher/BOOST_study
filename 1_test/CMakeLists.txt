cmake_minimum_required(VERSION 3.2)

project(test)

set(Boost_INCLUDE_DIR F:/boost_build/include/boost-1_85)
set(Boost_LIBRARY_DIR F:/boost_build/lib)
set(Boost_USE_STATIC_LIBS ON)

find_package(Boost REQUIRED)

include_directories(${Boost_INCLUDE_DIR})
link_directories(${Boost_LIBRARY_DIR})

set(SOURCES
    src/main.cpp
)

add_executable(test ${SOURCES})
target_link_libraries( test ${Boost_LIBRARIES} )
target_include_directories(test PRIVATE .)