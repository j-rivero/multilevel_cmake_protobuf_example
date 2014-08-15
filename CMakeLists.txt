cmake_minimum_required(VERSION 2.8)
project(protobuf_test)

# The drama is well documented in:
# http://stackoverflow.com/questions/19343018/cmake-and-findprotobuf 

find_package(Protobuf REQUIRED)
add_subdirectory(msg)
add_subdirectory(src)
