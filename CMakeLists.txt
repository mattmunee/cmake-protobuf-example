project(rpc)
cmake_minimum_required(VERSION 3.4)

add_subdirectory(proto)

find_package(Protobuf REQUIRED)
include_directories(${Protobuf_INCLUDE_DIRS})
include_directories(${CMAKE_CURRENT_BINARY_DIR})
add_executable(main main.cpp)
target_link_libraries(main proto ${Protobuf_LIBRARIES})





