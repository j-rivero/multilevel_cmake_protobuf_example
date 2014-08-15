message(STATUS "Other subdir level: ${PROTOBUF_INCLUDE_DIRS}")
# Needed if use in libraries or headers
set_source_files_properties(${PROTO_SRC} ${PROTO_HEADER} PROPERTIES
                            GENERATED TRUE)
include_directories(${CMAKE_BINARY_DIR}/msg)
add_executable(test test.cc)
add_dependencies(test protobuf_compilation)
