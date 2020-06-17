cmake_minimum_required(VERSION 3.15)

project(protobuf_example)
set(CMAKE_CXX_STANDARD 11)
find_package(Protobuf REQUIRED)
include_directories(${Protobuf_INCLUDE_DIRS})
include_directories(${CMAKE_CURRENT_BINARY_DIR})

protobuf_generate_cpp(PROTO_SRCS PROTO_HDRS addressbook.proto)

add_executable(write
        ${PROTO_SRCS}
        ${PROTO_HDRS}
        write.cpp)
target_link_libraries(write ${Protobuf_LIBRARIES})

add_executable(read
        ${PROTO_SRCS}
        ${PROTO_HDRS}
        read.cpp)
target_link_libraries(read ${Protobuf_LIBRARIES})
