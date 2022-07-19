find_package(Protobuf REQUIRED)
include_directories(${Protobuf_INCLUDE_DIRS})
protobuf_generate_cpp(PROTO_SRCS PROTO_HDRS message.proto)
add_library(proto STATIC ${PROTO_SRCS} ${PROTO_HDRS})
