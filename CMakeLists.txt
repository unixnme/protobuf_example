cmake_minimum_required(VERSION 3.15)

project(protobuf_example)
set(CMAKE_CXX_STANDARD 11)
add_subdirectory(protobuf/cmake)

add_executable(write
        addressbook.pb.cc
        write.cpp)
target_link_libraries(write protobuf)

add_executable(read
        addressbook.pb.cc
        read.cpp)
target_link_libraries(read protobuf)
