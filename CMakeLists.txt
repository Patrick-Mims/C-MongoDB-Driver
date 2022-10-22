cmake_minimum_required(VERSION 3.24)

set(PROJECT main)

project(${PROJECT} VERSION 1.0 DESCRIPTION "MongoDB C Driver Build File" LANGUAGES C HOMEPAGE_URL "https://www.bam.net")

include_directories("/usr/include/libbson-1.0")
include_directories("/usr/include/libmongoc-1.0")

add_executable(${PROJECT} src/client.c)

target_link_libraries(${PROJECT} /usr/lib/x86_64-linux-gnu/libmongoc-1.0.so.0 /usr/lib/x86_64-linux-gnu/libbson-1.0.so.0)
