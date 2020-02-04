cmake_minimum_required(VERSION 3.0.0)
project(template_link C)

include("${CMAKE_CURRENT_LIST_DIR}/dslink/CMakeLists.txt")
include_directories("include")

set(SRC "src/main.c" "src/invoke.c" "src/replicator.c" "src/rng.c")

add_executable(link ${SRC})
add_dependencies(link sdk_dslink_c-static)
target_link_libraries(link sdk_dslink_c-static)
