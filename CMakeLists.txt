cmake_minimum_required(VERSION 3.6)
project("clinfo")

set(CMAKE_CXX_STANDARD 17)

include_directories(
    3rdparty/OpenCL-Headers
)

file(GLOB clinfo_srcs
    "src/*.c"
    "src/opencl_wrapper/opencl_wrapper.cc"
)

add_executable(${PROJECT_NAME} ${clinfo_srcs})
