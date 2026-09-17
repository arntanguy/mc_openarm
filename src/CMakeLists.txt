configure_file(openarm.in.cpp "${CMAKE_CURRENT_BINARY_DIR}/openarm.cpp")

set(openarm_SRC "${CMAKE_CURRENT_BINARY_DIR}/openarm.cpp")
set(openarm_HDR openarm.h)

add_robot(openarm ${openarm_SRC} ${openarm_HDR})
target_include_directories(openarm PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}")
