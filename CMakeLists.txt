cmake_minimum_required(VERSION 3.5)
project(crawl CXX C)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror -I/usr/include/libxml2")

set(CMAKE_C_STANDARD 11)

include_directories(.)
include_directories(lib)

add_executable(crawl
    crawl.cpp)

find_package(CURL REQUIRED)
find_package(LibXml2 REQUIRED)

target_link_libraries(crawl
    curl
    ${LIBXML2_LIBRARIES})

